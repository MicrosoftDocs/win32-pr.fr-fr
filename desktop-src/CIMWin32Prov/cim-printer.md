---
description: La \_ classe d’imprimantes CIM représente les fonctionnalités et la gestion de l’unité logique d’imprimante.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: Classe CIM_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111542"
---
# <a name="cim_printer-class"></a><span data-ttu-id="ce10f-103">\_Classe d’imprimantes CIM</span><span class="sxs-lookup"><span data-stu-id="ce10f-103">CIM\_Printer class</span></span>

<span data-ttu-id="ce10f-104">La classe d' **\_ imprimantes CIM** représente les fonctionnalités et la gestion de l’unité logique d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce10f-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ce10f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce10f-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ce10f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ce10f-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ce10f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ce10f-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ce10f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce10f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce10f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="ce10f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ce10f-110">Members</span></span>

<span data-ttu-id="ce10f-111">La classe d' **\_ imprimantes CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ce10f-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="ce10f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ce10f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ce10f-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ce10f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ce10f-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ce10f-114">Methods</span></span>

<span data-ttu-id="ce10f-115">La classe d' **\_ imprimante CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ce10f-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="ce10f-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="ce10f-116">Method</span></span>                                                             | <span data-ttu-id="ce10f-117">Description</span><span class="sxs-lookup"><span data-stu-id="ce10f-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce10f-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="ce10f-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="ce10f-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ce10f-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="ce10f-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="ce10f-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="ce10f-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ce10f-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="ce10f-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="ce10f-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ce10f-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="ce10f-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ce10f-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ce10f-124">Properties</span></span>

<span data-ttu-id="ce10f-125">La classe d' **\_ imprimante CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ce10f-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce10f-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="ce10f-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-130">Availability and status of the device.</span></span>

<span data-ttu-id="ce10f-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ce10f-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-135">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="ce10f-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ce10f-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ce10f-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ce10f-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ce10f-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ce10f-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ce10f-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ce10f-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ce10f-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ce10f-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ce10f-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-146">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="ce10f-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ce10f-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-148">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="ce10f-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ce10f-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-150">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ce10f-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ce10f-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-153">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ce10f-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ce10f-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-155">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="ce10f-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ce10f-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-157">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="ce10f-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ce10f-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-159">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="ce10f-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ce10f-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-161">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="ce10f-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-162">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="ce10f-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-163">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-165">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="ce10f-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-166">Décrit toutes les feuilles de travail disponibles sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="ce10f-167">Cela peut également être utilisé pour décrire la bannière qu’une imprimante peut fournir au début de chaque travail, ou peut décrire d’autres options spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce10f-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-168">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ce10f-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-169">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-171">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**. CapabilityDescriptions "," CIM \_ PrintJob. finition "," CIM \_ printservice. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-172">Fonctionnalités de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="ce10f-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="ce10f-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="ce10f-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="ce10f-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="ce10f-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="ce10f-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="ce10f-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="ce10f-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="ce10f-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="ce10f-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="ce10f-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-186">Un côté</span><span class="sxs-lookup"><span data-stu-id="ce10f-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="ce10f-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-188">Bord long recto verso</span><span class="sxs-lookup"><span data-stu-id="ce10f-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="ce10f-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-190">Bord abrégé recto verso</span><span class="sxs-lookup"><span data-stu-id="ce10f-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="ce10f-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="ce10f-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="ce10f-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="ce10f-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="ce10f-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-196">Qualité élevée</span><span class="sxs-lookup"><span data-stu-id="ce10f-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="ce10f-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-198">Qualité normale</span><span class="sxs-lookup"><span data-stu-id="ce10f-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="ce10f-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-200">Qualité faible</span><span class="sxs-lookup"><span data-stu-id="ce10f-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-201">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ce10f-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-202">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-204">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="ce10f-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-205">Chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités de l’imprimante indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="ce10f-206">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="ce10f-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce10f-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ce10f-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-210">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-211">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ce10f-211">Short textual description of the object.</span></span>

<span data-ttu-id="ce10f-212">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-213">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-214">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-216">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Imprimante IETF-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-217">Jeux de caractères disponibles pour la sortie de texte relative à la gestion de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="ce10f-218">Les chaînes fournies dans cette propriété doivent être conformes à la sémantique et à la syntaxe spécifiées par la section 4.1.2 ("charset Parameter") dans la norme RFC 2046 (MIME part 2) et contenues dans le registre des jeux de caractères IANA.</span><span class="sxs-lookup"><span data-stu-id="ce10f-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="ce10f-219">Exemples : « UTF-8 », « US-ASCII » et « ISO-8859-1 ».</span><span class="sxs-lookup"><span data-stu-id="ce10f-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ce10f-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-221">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-223">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ce10f-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-224">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="ce10f-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ce10f-225">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ce10f-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ce10f-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-228">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ce10f-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ce10f-230">(1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-231">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ce10f-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ce10f-233">(2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ce10f-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ce10f-235">(3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-236">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="ce10f-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ce10f-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ce10f-238">(4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-239">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-239">Device is not working properly.</span></span> <span data-ttu-id="ce10f-240">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="ce10f-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ce10f-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ce10f-242">(5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-243">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="ce10f-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ce10f-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ce10f-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-246">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="ce10f-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ce10f-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ce10f-248">(7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ce10f-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ce10f-250">(8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-251">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="ce10f-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ce10f-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ce10f-253">(9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-254">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-254">Device is not working properly.</span></span> <span data-ttu-id="ce10f-255">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ce10f-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ce10f-257">(10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-258">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ce10f-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ce10f-260">(11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-261">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ce10f-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ce10f-263">douze</span><span class="sxs-lookup"><span data-stu-id="ce10f-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-264">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ce10f-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ce10f-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ce10f-266">(13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-267">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ce10f-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ce10f-269">(14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-270">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="ce10f-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ce10f-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ce10f-272">(15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-273">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="ce10f-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ce10f-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ce10f-275">(16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-276">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ce10f-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ce10f-278">(17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-279">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="ce10f-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ce10f-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ce10f-281">(18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-282">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="ce10f-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ce10f-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ce10f-284">(19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ce10f-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ce10f-286">(20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-287">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="ce10f-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ce10f-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ce10f-289">(21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-290">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="ce10f-290">System failure.</span></span> <span data-ttu-id="ce10f-291">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="ce10f-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ce10f-292">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ce10f-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ce10f-294">(22)</span><span class="sxs-lookup"><span data-stu-id="ce10f-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-295">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ce10f-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ce10f-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ce10f-297">(23)</span><span class="sxs-lookup"><span data-stu-id="ce10f-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-298">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="ce10f-298">System failure.</span></span> <span data-ttu-id="ce10f-299">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="ce10f-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ce10f-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ce10f-301">(24)</span><span class="sxs-lookup"><span data-stu-id="ce10f-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-302">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="ce10f-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ce10f-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ce10f-304">(25)</span><span class="sxs-lookup"><span data-stu-id="ce10f-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-305">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ce10f-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ce10f-307">(26)</span><span class="sxs-lookup"><span data-stu-id="ce10f-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-308">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ce10f-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ce10f-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ce10f-310">(27)</span><span class="sxs-lookup"><span data-stu-id="ce10f-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-311">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="ce10f-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ce10f-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ce10f-313">(28)</span><span class="sxs-lookup"><span data-stu-id="ce10f-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-314">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="ce10f-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ce10f-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ce10f-316">(29)</span><span class="sxs-lookup"><span data-stu-id="ce10f-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-317">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ce10f-317">Device is disabled.</span></span> <span data-ttu-id="ce10f-318">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="ce10f-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ce10f-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ce10f-320">(30)</span><span class="sxs-lookup"><span data-stu-id="ce10f-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-321">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="ce10f-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ce10f-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="ce10f-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ce10f-323">31</span><span class="sxs-lookup"><span data-stu-id="ce10f-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-324">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-324">Device is not working properly.</span></span> <span data-ttu-id="ce10f-325">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="ce10f-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-326">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="ce10f-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-327">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ce10f-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-329">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ce10f-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-330">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ce10f-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ce10f-331">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ce10f-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-335">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ce10f-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-336">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="ce10f-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ce10f-337">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="ce10f-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ce10f-338">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-339">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ce10f-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-340">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-342">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="ce10f-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-343">Les finitions et les autres fonctionnalités de l’imprimante en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ce10f-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="ce10f-344">Chaque entrée de cette propriété doit également être listée dans le tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="ce10f-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="ce10f-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="ce10f-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="ce10f-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="ce10f-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="ce10f-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="ce10f-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="ce10f-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="ce10f-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="ce10f-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="ce10f-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-358">Un côté</span><span class="sxs-lookup"><span data-stu-id="ce10f-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="ce10f-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-360">Bord long recto verso</span><span class="sxs-lookup"><span data-stu-id="ce10f-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="ce10f-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-362">Bord abrégé recto verso</span><span class="sxs-lookup"><span data-stu-id="ce10f-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="ce10f-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="ce10f-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="ce10f-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="ce10f-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="ce10f-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-368">Qualité élevée</span><span class="sxs-lookup"><span data-stu-id="ce10f-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="ce10f-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-370">Qualité normale</span><span class="sxs-lookup"><span data-stu-id="ce10f-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="ce10f-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-372">Qualité faible</span><span class="sxs-lookup"><span data-stu-id="ce10f-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-373">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="ce10f-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-376">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-377">Jeu de caractères actuel utilisé pour la sortie de texte relative à la gestion de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="ce10f-378">Le jeu de caractères décrit par cette propriété doit également être répertorié dans la propriété **CharsetsSupported** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="ce10f-379">La chaîne spécifiée par cette propriété doit être conforme à la sémantique et à la syntaxe spécifiées par la section 4.1.2 ("charset Parameter") dans la norme RFC 2046 (MIME part 2) et contenue dans le Registre du jeu de caractères IANA.</span><span class="sxs-lookup"><span data-stu-id="ce10f-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="ce10f-380">Exemples : « UTF-8 », « US-ASCII » et « ISO-8859-1 ».</span><span class="sxs-lookup"><span data-stu-id="ce10f-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-381">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="ce10f-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-382">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-384">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**. LanguagesSupported "," CIM \_ Printer. CurrentMimeType ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-385">Langue actuellement utilisée pour l’imprimante ; la langue doit également être indiquée dans la propriété **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-386">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-387">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="ce10f-388">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="ce10f-389">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="ce10f-390">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="ce10f-391">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="ce10f-392">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="ce10f-393">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="ce10f-394">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="ce10f-395">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="ce10f-396">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="ce10f-397">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="ce10f-398">**Interpression** (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="ce10f-399">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="ce10f-400">**Données de ligne** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="ce10f-401">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="ce10f-402">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="ce10f-403">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="ce10f-404">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="ce10f-405">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="ce10f-406">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="ce10f-407">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="ce10f-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="ce10f-408">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="ce10f-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="ce10f-409">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="ce10f-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="ce10f-410">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="ce10f-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="ce10f-411">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="ce10f-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="ce10f-412">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="ce10f-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="ce10f-413">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="ce10f-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="ce10f-414">**Pression positive** (29)</span><span class="sxs-lookup"><span data-stu-id="ce10f-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="ce10f-415">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="ce10f-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="ce10f-416">**Texte simple** (31)</span><span class="sxs-lookup"><span data-stu-id="ce10f-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="ce10f-417">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="ce10f-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="ce10f-418">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="ce10f-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="ce10f-419">**impressionne** (34)</span><span class="sxs-lookup"><span data-stu-id="ce10f-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="ce10f-420">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="ce10f-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="ce10f-421">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="ce10f-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="ce10f-422">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="ce10f-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ce10f-423">**Automatique** (38)</span><span class="sxs-lookup"><span data-stu-id="ce10f-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="ce10f-424">**Pages** (39)</span><span class="sxs-lookup"><span data-stu-id="ce10f-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="ce10f-425">**Lèvres** (40)</span><span class="sxs-lookup"><span data-stu-id="ce10f-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="ce10f-426">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="ce10f-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ce10f-427">**Diagnostic** (42)</span><span class="sxs-lookup"><span data-stu-id="ce10f-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="ce10f-428">**Majuscules** (43)</span><span class="sxs-lookup"><span data-stu-id="ce10f-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="ce10f-429">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="ce10f-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="ce10f-430">**Écrans plats** (45)</span><span class="sxs-lookup"><span data-stu-id="ce10f-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="ce10f-431">**X** (46)</span><span class="sxs-lookup"><span data-stu-id="ce10f-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="ce10f-432">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="ce10f-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-433">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="ce10f-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-436">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-437">Type MIME actuellement utilisé par l’imprimante lorsque la propriété **currentLanguage** est définie pour indiquer qu’un type MIME est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ce10f-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-438">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="ce10f-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-441">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-442">Langue actuelle utilisée par l’imprimante pour la gestion.</span><span class="sxs-lookup"><span data-stu-id="ce10f-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="ce10f-443">La langue répertoriée ici doit également être répertoriée dans **NaturalLanguagesSupported**.</span><span class="sxs-lookup"><span data-stu-id="ce10f-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-444">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="ce10f-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-447">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-448">Type de papier actuellement utilisé par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="ce10f-449">La chaîne doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 10175 (DPA), qui est également résumée dans l’annexe C de la RFC 1759 (MIB de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="ce10f-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-450">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ce10f-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-451">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-453">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="ce10f-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-454">Les finitions par défaut et d’autres fonctionnalités de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="ce10f-455">Chaque entrée de cette propriété doit également être listée dans le tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="ce10f-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="ce10f-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="ce10f-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="ce10f-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="ce10f-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="ce10f-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="ce10f-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="ce10f-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="ce10f-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="ce10f-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="ce10f-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-469">Un côté</span><span class="sxs-lookup"><span data-stu-id="ce10f-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="ce10f-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-471">Bord long recto verso</span><span class="sxs-lookup"><span data-stu-id="ce10f-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="ce10f-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-473">Bord abrégé recto verso</span><span class="sxs-lookup"><span data-stu-id="ce10f-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="ce10f-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="ce10f-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="ce10f-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="ce10f-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="ce10f-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-479">Qualité élevée</span><span class="sxs-lookup"><span data-stu-id="ce10f-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="ce10f-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-481">Qualité normale</span><span class="sxs-lookup"><span data-stu-id="ce10f-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="ce10f-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-483">Qualité faible</span><span class="sxs-lookup"><span data-stu-id="ce10f-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-484">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="ce10f-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-485">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-487">Nombre de copies qu’un seul travail produira, sauf spécification contraire.</span><span class="sxs-lookup"><span data-stu-id="ce10f-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="ce10f-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-489">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-490">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-491">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**. LanguagesSupported "," CIM \_ Printer. DefaultMimeType ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-492">Langue de l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce10f-492">Default printer language.</span></span> <span data-ttu-id="ce10f-493">La langue doit également être indiquée dans la propriété **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-494">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-495">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="ce10f-496">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="ce10f-497">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="ce10f-498">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="ce10f-499">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="ce10f-500">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="ce10f-501">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="ce10f-502">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="ce10f-503">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="ce10f-504">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="ce10f-505">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="ce10f-506">**Interpression** (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="ce10f-507">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="ce10f-508">**Données de ligne** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="ce10f-509">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="ce10f-510">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="ce10f-511">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="ce10f-512">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="ce10f-513">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="ce10f-514">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="ce10f-515">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="ce10f-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="ce10f-516">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="ce10f-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="ce10f-517">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="ce10f-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="ce10f-518">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="ce10f-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="ce10f-519">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="ce10f-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="ce10f-520">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="ce10f-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="ce10f-521">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="ce10f-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="ce10f-522">**Pression positive** (29)</span><span class="sxs-lookup"><span data-stu-id="ce10f-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="ce10f-523">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="ce10f-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="ce10f-524">**Texte simple** (31)</span><span class="sxs-lookup"><span data-stu-id="ce10f-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="ce10f-525">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="ce10f-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="ce10f-526">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="ce10f-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="ce10f-527">**impressionne** (34)</span><span class="sxs-lookup"><span data-stu-id="ce10f-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="ce10f-528">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="ce10f-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="ce10f-529">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="ce10f-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="ce10f-530">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="ce10f-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ce10f-531">**Automatique** (38)</span><span class="sxs-lookup"><span data-stu-id="ce10f-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="ce10f-532">**Pages** (39)</span><span class="sxs-lookup"><span data-stu-id="ce10f-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="ce10f-533">**Lèvres** (40)</span><span class="sxs-lookup"><span data-stu-id="ce10f-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="ce10f-534">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="ce10f-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ce10f-535">**Diagnostic** (42)</span><span class="sxs-lookup"><span data-stu-id="ce10f-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="ce10f-536">**Majuscules** (43)</span><span class="sxs-lookup"><span data-stu-id="ce10f-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="ce10f-537">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="ce10f-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="ce10f-538">**Écrans plats** (45)</span><span class="sxs-lookup"><span data-stu-id="ce10f-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="ce10f-539">**X** (46)</span><span class="sxs-lookup"><span data-stu-id="ce10f-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="ce10f-540">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="ce10f-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-541">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="ce10f-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-542">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-543">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-544">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-545">Type MIME par défaut utilisé par l’imprimante lorsque la propriété **DefaultLanguage** est définie pour indiquer qu’un type MIME est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ce10f-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-546">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="ce10f-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-547">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-549">Nombre de pages de flux d’impression que l’imprimante rendra sur une seule feuille de média, sauf si une tâche le spécifie autrement.</span><span class="sxs-lookup"><span data-stu-id="ce10f-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-550">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="ce10f-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-551">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-552">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-553">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-554">Type de papier que l’imprimante utilisera si PrintJob ne spécifie pas un type particulier.</span><span class="sxs-lookup"><span data-stu-id="ce10f-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="ce10f-555">La chaîne doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 10175 (DPA), qui est également résumée dans l’annexe C de la RFC 1759 (MIB de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="ce10f-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-556">**Description**</span><span class="sxs-lookup"><span data-stu-id="ce10f-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-557">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-558">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-559">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ce10f-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-560">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ce10f-560">Textual description of the object.</span></span>

<span data-ttu-id="ce10f-561">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-562">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="ce10f-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-563">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-564">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-565">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. \|Imprimante IETF-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-566">Informations sur l’erreur de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-567">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-568">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="ce10f-569">**Aucune erreur** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="ce10f-570">**Papier faible** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="ce10f-571">**Aucun papier** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="ce10f-572">**Toner faible** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="ce10f-573">**Aucun toner** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="ce10f-574">**Porte ouverte** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="ce10f-575">**Coincé** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="ce10f-576">**Hors connexion** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="ce10f-577">**Service demandé** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="ce10f-578">**Bac de sortie complet** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-579">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ce10f-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-580">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-581">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-582">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ce10f-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-583">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ce10f-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="ce10f-584">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-585">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ce10f-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-586">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ce10f-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-587">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-588">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="ce10f-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="ce10f-589">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ce10f-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-591">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-592">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-593">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="ce10f-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="ce10f-594">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-595">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="ce10f-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-596">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-597">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ce10f-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-598">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**.**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="ce10f-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-599">Tableau qui fournit des informations supplémentaires sur l’état d’erreur actuel, indiqué dans la propriété **DetectedErrorState** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="ce10f-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-601">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-602">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-603">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels par pouce")</span><span class="sxs-lookup"><span data-stu-id="ce10f-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-604">Résolution horizontale en pixels par pouce.</span><span class="sxs-lookup"><span data-stu-id="ce10f-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ce10f-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-606">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ce10f-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-607">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-608">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-609">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ce10f-609">Date and time the object was installed.</span></span> <span data-ttu-id="ce10f-610">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="ce10f-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ce10f-611">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-612">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="ce10f-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-613">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-614">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-615">Qualificateurs : **compteur**</span><span class="sxs-lookup"><span data-stu-id="ce10f-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-616">Travaux d’impression traités depuis la dernière réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="ce10f-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="ce10f-617">Ces travaux peuvent être traités à partir d’une ou de plusieurs files d’attente d’impression.</span><span class="sxs-lookup"><span data-stu-id="ce10f-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-618">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-619">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-620">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-621">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Imprimante IETF-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**. MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ printservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-622">Langues d’impression prises en charge en mode natif.</span><span class="sxs-lookup"><span data-stu-id="ce10f-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-623">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-624">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="ce10f-625">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="ce10f-626">**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="ce10f-627">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="ce10f-628">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="ce10f-629">**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="ce10f-630">**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="ce10f-631">**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="ce10f-632">**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="ce10f-633">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="ce10f-634">**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="ce10f-635">**Interpression** (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="ce10f-636">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="ce10f-637">**Données de ligne** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="ce10f-638">**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="ce10f-639">**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="ce10f-640">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="ce10f-641">**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="ce10f-642">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="ce10f-643">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="ce10f-644">**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="ce10f-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="ce10f-645">**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="ce10f-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="ce10f-646">**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="ce10f-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="ce10f-647">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="ce10f-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="ce10f-648">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="ce10f-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="ce10f-649">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="ce10f-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="ce10f-650">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="ce10f-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="ce10f-651">**Pression positive** (29)</span><span class="sxs-lookup"><span data-stu-id="ce10f-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="ce10f-652">**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="ce10f-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="ce10f-653">**Texte simple** (31)</span><span class="sxs-lookup"><span data-stu-id="ce10f-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="ce10f-654">**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="ce10f-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="ce10f-655">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="ce10f-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="ce10f-656">**impressionne** (34)</span><span class="sxs-lookup"><span data-stu-id="ce10f-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="ce10f-657">**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="ce10f-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="ce10f-658">**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="ce10f-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="ce10f-659">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="ce10f-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ce10f-660">**Automatique** (38)</span><span class="sxs-lookup"><span data-stu-id="ce10f-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="ce10f-661">**Pages** (39)</span><span class="sxs-lookup"><span data-stu-id="ce10f-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="ce10f-662">**Lèvres** (40)</span><span class="sxs-lookup"><span data-stu-id="ce10f-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="ce10f-663">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="ce10f-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ce10f-664">**Diagnostic** (42)</span><span class="sxs-lookup"><span data-stu-id="ce10f-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="ce10f-665">**Majuscules** (43)</span><span class="sxs-lookup"><span data-stu-id="ce10f-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="ce10f-666">**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="ce10f-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="ce10f-667">**Écrans plats** (45)</span><span class="sxs-lookup"><span data-stu-id="ce10f-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="ce10f-668">**X** (46)</span><span class="sxs-lookup"><span data-stu-id="ce10f-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="ce10f-669">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="ce10f-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="ce10f-670">**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="ce10f-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="ce10f-671">**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="ce10f-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="ce10f-672">**Pclxl** (50)</span><span class="sxs-lookup"><span data-stu-id="ce10f-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-673">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ce10f-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-674">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-675">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-676">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ce10f-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ce10f-677">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-678">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="ce10f-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-679">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-680">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-681">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Imprimante IETF-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-682">Technologie de marquage utilisée par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-683">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-684">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="ce10f-685">**LED électrophotographique** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="ce10f-686">**Laser électrophotographique** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="ce10f-687">**Électrophotographique autre** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="ce10f-688">**Impact sur le déplacement de la matrice point-tête 9** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="ce10f-689">**Impact sur le déplacement de la matrice point-tête 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="ce10f-690">**Impact-déplacement de la matrice des points en-tête** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="ce10f-691">**Impact du déplacement de la tête en forme complète** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="ce10f-692">**Bande d’impact** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="ce10f-693">**Impact sur Other** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="ce10f-694">**Jet d’encre aqueux** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="ce10f-695">**Jet d’encre solide** (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="ce10f-696">**Autre encre** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="ce10f-697">**Stylet** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="ce10f-698">**Transfert thermique** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="ce10f-699">**Sensibilité thermique** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="ce10f-700">**Diffusion thermique** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="ce10f-701">**Autre température** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="ce10f-702">**Electroerosion** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="ce10f-703">**Électrostatique** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="ce10f-704">**Microfiche photographique** (22)</span><span class="sxs-lookup"><span data-stu-id="ce10f-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="ce10f-705">**Photocomposeuse photo** (23)</span><span class="sxs-lookup"><span data-stu-id="ce10f-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="ce10f-706">**Photographie autre** (24)</span><span class="sxs-lookup"><span data-stu-id="ce10f-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="ce10f-707">**Déposition d’ions** (25)</span><span class="sxs-lookup"><span data-stu-id="ce10f-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="ce10f-708">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="ce10f-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="ce10f-709">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="ce10f-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-710">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="ce10f-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-711">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-712">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-713">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. copies")</span><span class="sxs-lookup"><span data-stu-id="ce10f-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-714">Nombre maximal de copies qui peuvent être produites par l’imprimante à partir d’un seul travail.</span><span class="sxs-lookup"><span data-stu-id="ce10f-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-715">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="ce10f-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-716">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-717">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-718">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="ce10f-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-719">Nombre maximal de pages de flux d’impression que l’imprimante peut afficher sur une seule feuille de média.</span><span class="sxs-lookup"><span data-stu-id="ce10f-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-720">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-721">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-722">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-723">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (« CIM \_ PrintJob. Jobs »), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-724">Travail le plus volumineux (sous la forme d’un flux d’octets) accepté par l’imprimante en unités de kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="ce10f-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="ce10f-725">La valeur 0 (zéro) indique qu’aucune limite n’a été définie.</span><span class="sxs-lookup"><span data-stu-id="ce10f-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-726">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-727">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-728">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-729">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ imprimante CIM**. LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ printservice. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-730">Chaînes de forme libre qui fournissent des explications détaillées sur les types MIME pris en charge par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="ce10f-731">Si des données sont fournies pour cette propriété, la valeur 47 (« MIME ») doit être incluse dans la propriété **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-732">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ce10f-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-733">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-734">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-735">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ce10f-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-736">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="ce10f-736">Label by which the object is known.</span></span> <span data-ttu-id="ce10f-737">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="ce10f-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ce10f-738">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-739">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-740">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-741">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-742">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Imprimante IETF-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-743">Langues disponibles pour les chaînes utilisées par l’imprimante pour la sortie des informations de gestion.</span><span class="sxs-lookup"><span data-stu-id="ce10f-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="ce10f-744">Les chaînes doivent être conformes à la norme RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="ce10f-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="ce10f-745">Par exemple, « fr » est utilisé pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="ce10f-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-746">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-747">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-748">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-749">Types de papier pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ce10f-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-750">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-751">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="ce10f-752">**A** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="ce10f-753">**B** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="ce10f-754">**C** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="ce10f-755">**D** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="ce10f-756">**E** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="ce10f-757">**Lettre** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="ce10f-758">**Légal** (8)</span><span class="sxs-lookup"><span data-stu-id="ce10f-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="ce10f-759">**Na-10x13-Envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="ce10f-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="ce10f-760">**Na-9x12-Envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="ce10f-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="ce10f-761">**Na-Number-10-enveloppe** (11)</span><span class="sxs-lookup"><span data-stu-id="ce10f-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="ce10f-762">**Na-7x9-Envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="ce10f-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="ce10f-763">**Na-9x11-Envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="ce10f-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="ce10f-764">**Na-10x14-Envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="ce10f-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="ce10f-765">**Na-Number-9-enveloppe** (15)</span><span class="sxs-lookup"><span data-stu-id="ce10f-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="ce10f-766">**Na-6x9-Envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="ce10f-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="ce10f-767">**Na-10x15-Envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="ce10f-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="ce10f-768">**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="ce10f-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="ce10f-769">**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="ce10f-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="ce10f-770">**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="ce10f-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="ce10f-771">**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="ce10f-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="ce10f-772">**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="ce10f-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="ce10f-773">**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="ce10f-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="ce10f-774">**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="ce10f-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="ce10f-775">**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="ce10f-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="ce10f-776">**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="ce10f-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="ce10f-777">**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="ce10f-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="ce10f-778">**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="ce10f-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="ce10f-779">**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="ce10f-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="ce10f-780">**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="ce10f-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="ce10f-781">**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="ce10f-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="ce10f-782">**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="ce10f-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="ce10f-783">**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="ce10f-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="ce10f-784">**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="ce10f-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="ce10f-785">**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="ce10f-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="ce10f-786">**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="ce10f-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="ce10f-787">**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="ce10f-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="ce10f-788">**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="ce10f-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="ce10f-789">**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="ce10f-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="ce10f-790">**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="ce10f-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="ce10f-791">**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="ce10f-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="ce10f-792">**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="ce10f-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="ce10f-793">**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="ce10f-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="ce10f-794">**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="ce10f-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="ce10f-795">**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="ce10f-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="ce10f-796">**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="ce10f-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="ce10f-797">**Désignée ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="ce10f-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="ce10f-798">**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="ce10f-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="ce10f-799">**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="ce10f-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="ce10f-800">**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="ce10f-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="ce10f-801">**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="ce10f-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="ce10f-802">**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="ce10f-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="ce10f-803">**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="ce10f-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="ce10f-804">**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="ce10f-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="ce10f-805">**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="ce10f-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="ce10f-806">**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="ce10f-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="ce10f-807">**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="ce10f-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="ce10f-808">**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="ce10f-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="ce10f-809">**Lettre na** (59)</span><span class="sxs-lookup"><span data-stu-id="ce10f-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="ce10f-810">**Na-Legal** (60)</span><span class="sxs-lookup"><span data-stu-id="ce10f-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="ce10f-811">**B4-enveloppe** (61)</span><span class="sxs-lookup"><span data-stu-id="ce10f-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="ce10f-812">**B5-enveloppe** (62)</span><span class="sxs-lookup"><span data-stu-id="ce10f-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="ce10f-813">**C3-enveloppe** (63)</span><span class="sxs-lookup"><span data-stu-id="ce10f-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="ce10f-814">**C4-enveloppe** (64)</span><span class="sxs-lookup"><span data-stu-id="ce10f-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="ce10f-815">**C5-enveloppe** (65)</span><span class="sxs-lookup"><span data-stu-id="ce10f-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="ce10f-816">**C6-enveloppe** (66)</span><span class="sxs-lookup"><span data-stu-id="ce10f-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="ce10f-817">**Enveloppe indiquée-long** (67)</span><span class="sxs-lookup"><span data-stu-id="ce10f-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="ce10f-818">**Monarch-enveloppe** (68)</span><span class="sxs-lookup"><span data-stu-id="ce10f-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="ce10f-819">**Executive** (69)</span><span class="sxs-lookup"><span data-stu-id="ce10f-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="ce10f-820">**Folio** (70)</span><span class="sxs-lookup"><span data-stu-id="ce10f-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="ce10f-821">**Facture** (71)</span><span class="sxs-lookup"><span data-stu-id="ce10f-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="ce10f-822">**Grand livre** (72)</span><span class="sxs-lookup"><span data-stu-id="ce10f-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="ce10f-823">**Papier Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="ce10f-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-824">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="ce10f-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-825">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ce10f-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-826">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-827">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ printservice. PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Imprimante IETF-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-828">Chaînes de forme libre qui spécifient les types de papier actuellement disponibles pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="ce10f-829">Chaque chaîne doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 10175 (DPA), qui est également résumée dans l’annexe C du RFC 1759 (MIB de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="ce10f-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="ce10f-830">Les exemples de chaînes valides sont « ISO-A4-Color » et « na-10x14-Envelope ».</span><span class="sxs-lookup"><span data-stu-id="ce10f-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="ce10f-831">Par définition, une taille de papier qui est disponible et répertoriée dans la propriété **PaperTypesAvailable** doit également apparaître dans la propriété **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ce10f-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-833">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-834">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-835">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ce10f-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-836">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="ce10f-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="ce10f-837">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ce10f-838">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="ce10f-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-839">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ce10f-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-840">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-841">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-842">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="ce10f-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ce10f-843">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="ce10f-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ce10f-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ce10f-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ce10f-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ce10f-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-848">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="ce10f-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ce10f-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-850">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="ce10f-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ce10f-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-852">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ce10f-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ce10f-853">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="ce10f-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ce10f-854">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="ce10f-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ce10f-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-856">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="ce10f-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ce10f-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ce10f-858">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="ce10f-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-859">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ce10f-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-860">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ce10f-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-861">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-862">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="ce10f-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="ce10f-863">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="ce10f-864">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ce10f-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="ce10f-865">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="ce10f-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="ce10f-866">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-867">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="ce10f-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-868">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-869">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-870">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Imprimante IETF-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-871">Informations d’État, au-delà de celles spécifiées dans la propriété **Availability** , pour une imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-872">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-873">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="ce10f-874">**Inactif** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="ce10f-875">**Impression** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="ce10f-876">**Préchauffage** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="ce10f-877">**Impression arrêtée** (6)</span><span class="sxs-lookup"><span data-stu-id="ce10f-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="ce10f-878">**Hors connexion** (7)</span><span class="sxs-lookup"><span data-stu-id="ce10f-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-879">**État**</span><span class="sxs-lookup"><span data-stu-id="ce10f-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-880">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-881">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-882">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ce10f-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-883">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ce10f-883">Current status of the object.</span></span> <span data-ttu-id="ce10f-884">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ce10f-885">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce10f-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ce10f-886">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ce10f-887">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ce10f-888">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-889">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="ce10f-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ce10f-890">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ce10f-891">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ce10f-892">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ce10f-893">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ce10f-894">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ce10f-895">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ce10f-896">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ce10f-897">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="ce10f-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ce10f-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-899">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce10f-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-900">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-901">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ce10f-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-902">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ce10f-902">State of the logical device.</span></span> <span data-ttu-id="ce10f-903">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="ce10f-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ce10f-904">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ce10f-905">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="ce10f-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ce10f-906">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="ce10f-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ce10f-907">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="ce10f-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ce10f-908">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="ce10f-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ce10f-909">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="ce10f-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce10f-910">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ce10f-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-911">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-912">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-913">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ce10f-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-914">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ce10f-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="ce10f-915">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-916">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ce10f-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-917">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ce10f-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-918">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-919">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ce10f-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-920">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ce10f-920">Scoping system's name.</span></span>

<span data-ttu-id="ce10f-921">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-922">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="ce10f-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-923">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ce10f-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-924">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-925">Heure de la dernière réinitialisation de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ce10f-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="ce10f-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="ce10f-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce10f-927">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce10f-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-928">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ce10f-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce10f-929">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels par pouce")</span><span class="sxs-lookup"><span data-stu-id="ce10f-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="ce10f-930">Résolution verticale en pixels par pouce.</span><span class="sxs-lookup"><span data-stu-id="ce10f-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce10f-931">Notes</span><span class="sxs-lookup"><span data-stu-id="ce10f-931">Remarks</span></span>

<span data-ttu-id="ce10f-932">La classe d' **\_ imprimante CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ce10f-933">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="ce10f-933">WMI does not implement this class.</span></span> <span data-ttu-id="ce10f-934">Pour la classe WMI dérivée de l' **\_ imprimante CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce10f-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ce10f-935">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ce10f-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce10f-936">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ce10f-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce10f-937">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce10f-937">Requirements</span></span>



| <span data-ttu-id="ce10f-938">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce10f-938">Requirement</span></span> | <span data-ttu-id="ce10f-939">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce10f-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce10f-940">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce10f-940">Minimum supported client</span></span><br/> | <span data-ttu-id="ce10f-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce10f-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce10f-942">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce10f-942">Minimum supported server</span></span><br/> | <span data-ttu-id="ce10f-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce10f-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce10f-944">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ce10f-944">Namespace</span></span><br/>                | <span data-ttu-id="ce10f-945">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ce10f-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce10f-946">MOF</span><span class="sxs-lookup"><span data-stu-id="ce10f-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce10f-947"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce10f-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce10f-948">DLL</span><span class="sxs-lookup"><span data-stu-id="ce10f-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce10f-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce10f-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce10f-950">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce10f-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce10f-951">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ce10f-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

