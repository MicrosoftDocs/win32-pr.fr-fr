---
description: La \_ classe CIM SerialController représente les fonctionnalités et la gestion de l’unité logique de port série.
ms.assetid: 7d5a96aa-fa6c-4904-8ca1-88ec14748810
ms.tgt_platform: multiple
title: CIM_SerialController, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Availability
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.Caption
- CIM_SerialController.ConfigManagerErrorCode
- CIM_SerialController.ConfigManagerUserConfig
- CIM_SerialController.CreationClassName
- CIM_SerialController.Description
- CIM_SerialController.DeviceID
- CIM_SerialController.ErrorCleared
- CIM_SerialController.ErrorDescription
- CIM_SerialController.InstallDate
- CIM_SerialController.LastErrorCode
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.MaxNumberControlled
- CIM_SerialController.Name
- CIM_SerialController.PNPDeviceID
- CIM_SerialController.PowerManagementCapabilities
- CIM_SerialController.PowerManagementSupported
- CIM_SerialController.ProtocolSupported
- CIM_SerialController.Status
- CIM_SerialController.StatusInfo
- CIM_SerialController.SystemCreationClassName
- CIM_SerialController.SystemName
- CIM_SerialController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e23c9183dabb9b4d9ea25f5f92bd4c8ec6667c04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543442"
---
# <a name="cim_serialcontroller-class-cimwin32-wmi-providers"></a><span data-ttu-id="613ac-103">CIM_SerialController, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="613ac-103">CIM_SerialController class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="613ac-104">La classe **CIM \_ SerialController** représente les fonctionnalités et la gestion de l’unité logique de port série.</span><span class="sxs-lookup"><span data-stu-id="613ac-104">The **CIM\_SerialController** class represents the capabilities and management of the serial port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="613ac-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="613ac-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="613ac-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="613ac-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="613ac-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="613ac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="613ac-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="613ac-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="613ac-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="613ac-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C554-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SerialController : CIM_Controller
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
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

## <a name="members"></a><span data-ttu-id="613ac-110">Membres</span><span class="sxs-lookup"><span data-stu-id="613ac-110">Members</span></span>

<span data-ttu-id="613ac-111">La classe **CIM \_ SerialController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="613ac-111">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="613ac-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="613ac-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="613ac-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="613ac-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="613ac-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="613ac-114">Methods</span></span>

<span data-ttu-id="613ac-115">La classe **CIM \_ SerialController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="613ac-115">The **CIM\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="613ac-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="613ac-116">Method</span></span>                                                                      | <span data-ttu-id="613ac-117">Description</span><span class="sxs-lookup"><span data-stu-id="613ac-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="613ac-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="613ac-118">**Reset**</span></span>](reset-method-in-class-cim-serialcontroller.md)                 | <span data-ttu-id="613ac-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="613ac-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="613ac-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="613ac-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="613ac-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="613ac-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-serialcontroller.md) | <span data-ttu-id="613ac-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="613ac-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="613ac-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="613ac-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="613ac-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="613ac-124">Properties</span></span>

<span data-ttu-id="613ac-125">La classe **CIM \_ SerialController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="613ac-125">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="613ac-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="613ac-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="613ac-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="613ac-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-130">Availability and status of the device.</span></span>

<span data-ttu-id="613ac-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="613ac-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="613ac-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="613ac-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="613ac-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="613ac-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="613ac-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="613ac-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="613ac-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="613ac-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="613ac-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="613ac-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="613ac-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="613ac-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="613ac-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="613ac-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="613ac-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="613ac-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="613ac-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="613ac-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="613ac-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="613ac-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="613ac-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="613ac-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="613ac-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="613ac-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="613ac-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="613ac-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="613ac-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="613ac-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="613ac-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="613ac-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="613ac-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-149">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="613ac-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="613ac-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="613ac-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="613ac-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="613ac-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="613ac-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="613ac-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="613ac-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="613ac-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="613ac-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="613ac-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="613ac-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="613ac-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="613ac-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="613ac-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="613ac-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="613ac-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="613ac-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="613ac-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-162">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="613ac-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="613ac-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-164">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ports série DMTF \| 004,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="613ac-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-165">Compatibilité au niveau du processeur pour le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="613ac-165">Chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="613ac-166">Cette propriété décrit la mise en mémoire tampon et d’autres fonctionnalités du contrôleur série, qui peuvent être inhérentes au matériel de puce.</span><span class="sxs-lookup"><span data-stu-id="613ac-166">This property describes buffering and other capabilities of the serial controller, that may be inherent in the chip hardware.</span></span> <span data-ttu-id="613ac-167">Cette propriété est un entier énuméré.</span><span class="sxs-lookup"><span data-stu-id="613ac-167">This property is an enumerated integer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="613ac-168">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="613ac-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="613ac-169">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="613ac-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="613ac-170">**Compatible XT/AT** (3)</span><span class="sxs-lookup"><span data-stu-id="613ac-170">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="613ac-171">**Compatible 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="613ac-171">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="613ac-172">**Compatible 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="613ac-172">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="613ac-173">**compatible 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="613ac-173">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="613ac-174">**Compatible 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="613ac-174">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="613ac-175">**compatible 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="613ac-175">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-176">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="613ac-176">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-177">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="613ac-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="613ac-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-179">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="613ac-179">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-180">Chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités du contrôleur série indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="613ac-180">Free-form strings that provide detailed explanations for the serial controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="613ac-181">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="613ac-181">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="613ac-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="613ac-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-185">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="613ac-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-186">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="613ac-186">Short textual description of the object.</span></span>

<span data-ttu-id="613ac-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="613ac-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-189">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613ac-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-191">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="613ac-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-192">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="613ac-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="613ac-193">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="613ac-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="613ac-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="613ac-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="613ac-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-196">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="613ac-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="613ac-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="613ac-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="613ac-198">(1)</span><span class="sxs-lookup"><span data-stu-id="613ac-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-199">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="613ac-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="613ac-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="613ac-201">(2)</span><span class="sxs-lookup"><span data-stu-id="613ac-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="613ac-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="613ac-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="613ac-203">(3)</span><span class="sxs-lookup"><span data-stu-id="613ac-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-204">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="613ac-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="613ac-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="613ac-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="613ac-206">(4)</span><span class="sxs-lookup"><span data-stu-id="613ac-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-207">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="613ac-207">Device is not working properly.</span></span> <span data-ttu-id="613ac-208">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="613ac-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="613ac-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="613ac-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="613ac-210">(5)</span><span class="sxs-lookup"><span data-stu-id="613ac-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-211">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="613ac-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="613ac-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="613ac-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="613ac-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="613ac-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-214">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="613ac-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="613ac-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="613ac-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="613ac-216">(7)</span><span class="sxs-lookup"><span data-stu-id="613ac-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="613ac-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="613ac-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="613ac-218">(8)</span><span class="sxs-lookup"><span data-stu-id="613ac-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-219">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="613ac-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="613ac-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="613ac-221">(9)</span><span class="sxs-lookup"><span data-stu-id="613ac-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-222">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="613ac-222">Device is not working properly.</span></span> <span data-ttu-id="613ac-223">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="613ac-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="613ac-225">(10)</span><span class="sxs-lookup"><span data-stu-id="613ac-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-226">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="613ac-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="613ac-228">(11)</span><span class="sxs-lookup"><span data-stu-id="613ac-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-229">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="613ac-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="613ac-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="613ac-231">douze</span><span class="sxs-lookup"><span data-stu-id="613ac-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-232">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="613ac-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="613ac-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="613ac-234">(13)</span><span class="sxs-lookup"><span data-stu-id="613ac-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-235">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="613ac-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="613ac-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="613ac-237">(14)</span><span class="sxs-lookup"><span data-stu-id="613ac-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-238">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="613ac-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="613ac-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="613ac-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="613ac-240">(15)</span><span class="sxs-lookup"><span data-stu-id="613ac-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-241">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="613ac-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="613ac-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="613ac-243">(16)</span><span class="sxs-lookup"><span data-stu-id="613ac-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-244">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="613ac-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="613ac-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="613ac-246">(17)</span><span class="sxs-lookup"><span data-stu-id="613ac-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-247">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="613ac-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="613ac-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="613ac-249">(18)</span><span class="sxs-lookup"><span data-stu-id="613ac-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-250">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="613ac-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="613ac-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="613ac-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="613ac-252">(19)</span><span class="sxs-lookup"><span data-stu-id="613ac-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="613ac-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="613ac-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="613ac-254">(20)</span><span class="sxs-lookup"><span data-stu-id="613ac-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-255">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="613ac-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="613ac-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="613ac-257">(21)</span><span class="sxs-lookup"><span data-stu-id="613ac-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-258">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="613ac-258">System failure.</span></span> <span data-ttu-id="613ac-259">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="613ac-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="613ac-260">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="613ac-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="613ac-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="613ac-262">(22)</span><span class="sxs-lookup"><span data-stu-id="613ac-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-263">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="613ac-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="613ac-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="613ac-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="613ac-265">(23)</span><span class="sxs-lookup"><span data-stu-id="613ac-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-266">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="613ac-266">System failure.</span></span> <span data-ttu-id="613ac-267">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="613ac-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="613ac-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="613ac-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="613ac-269">(24)</span><span class="sxs-lookup"><span data-stu-id="613ac-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-270">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="613ac-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="613ac-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="613ac-272">(25)</span><span class="sxs-lookup"><span data-stu-id="613ac-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-273">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="613ac-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="613ac-275">(26)</span><span class="sxs-lookup"><span data-stu-id="613ac-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-276">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="613ac-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="613ac-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="613ac-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="613ac-278">(27)</span><span class="sxs-lookup"><span data-stu-id="613ac-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-279">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="613ac-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="613ac-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="613ac-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="613ac-281">(28)</span><span class="sxs-lookup"><span data-stu-id="613ac-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-282">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="613ac-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="613ac-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="613ac-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="613ac-284">(29)</span><span class="sxs-lookup"><span data-stu-id="613ac-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-285">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="613ac-285">Device is disabled.</span></span> <span data-ttu-id="613ac-286">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="613ac-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="613ac-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="613ac-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="613ac-288">(30)</span><span class="sxs-lookup"><span data-stu-id="613ac-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-289">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="613ac-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="613ac-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="613ac-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="613ac-291">31</span><span class="sxs-lookup"><span data-stu-id="613ac-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-292">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="613ac-292">Device is not working properly.</span></span> <span data-ttu-id="613ac-293">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="613ac-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="613ac-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-295">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="613ac-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-297">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="613ac-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-298">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="613ac-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="613ac-299">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="613ac-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-303">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="613ac-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="613ac-304">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="613ac-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="613ac-305">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="613ac-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="613ac-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-307">**Description**</span><span class="sxs-lookup"><span data-stu-id="613ac-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-308">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-310">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="613ac-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-311">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="613ac-311">Textual description of the object.</span></span>

<span data-ttu-id="613ac-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="613ac-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-316">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="613ac-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="613ac-317">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="613ac-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="613ac-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="613ac-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-320">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="613ac-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613ac-322">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="613ac-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="613ac-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="613ac-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613ac-327">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="613ac-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="613ac-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-329">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="613ac-329">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-330">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="613ac-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-332">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="613ac-332">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-333">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="613ac-333">Date and time the object was installed.</span></span> <span data-ttu-id="613ac-334">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="613ac-334">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="613ac-335">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="613ac-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-337">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613ac-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613ac-339">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="613ac-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="613ac-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-341">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="613ac-341">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-342">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613ac-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-344">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ports série DMTF \| 004,6 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits par seconde ")</span><span class="sxs-lookup"><span data-stu-id="613ac-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-345">Débit en bauds maximal, en bits par seconde, pris en charge par le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="613ac-345">Maximum baud rate, in bits-per-second, supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="613ac-346">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="613ac-346">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-347">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613ac-347">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-349">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="613ac-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-350">Nombre maximal d’entités directement adressables prises en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="613ac-350">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="613ac-351">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="613ac-351">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="613ac-352">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-352">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-353">**Nom**</span><span class="sxs-lookup"><span data-stu-id="613ac-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-356">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="613ac-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-357">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="613ac-357">Label by which the object is known.</span></span> <span data-ttu-id="613ac-358">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="613ac-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="613ac-359">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-360">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="613ac-360">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-363">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="613ac-363">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-364">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="613ac-364">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="613ac-365">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="613ac-366">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="613ac-366">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="613ac-367">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="613ac-367">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-368">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="613ac-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="613ac-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613ac-370">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="613ac-370">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="613ac-371">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="613ac-371">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="613ac-372"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="613ac-372"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="613ac-373"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="613ac-373"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="613ac-374"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="613ac-374"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="613ac-375"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="613ac-375"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-376">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="613ac-376">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="613ac-377"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="613ac-377"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-378">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="613ac-378">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="613ac-379"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="613ac-379"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-380">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="613ac-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="613ac-381">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="613ac-381">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="613ac-382">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="613ac-382">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="613ac-383"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="613ac-383"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-384">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="613ac-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="613ac-385"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="613ac-385"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="613ac-386">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="613ac-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-387">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="613ac-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-388">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="613ac-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613ac-390">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="613ac-390">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="613ac-391">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="613ac-391">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="613ac-392">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="613ac-392">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="613ac-393">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="613ac-393">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="613ac-394">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-394">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-395">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="613ac-395">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-396">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="613ac-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-398">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="613ac-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-399">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="613ac-399">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="613ac-400">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-400">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="613ac-401">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="613ac-401">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="613ac-402">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="613ac-402">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="613ac-403">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="613ac-403">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="613ac-404">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="613ac-404">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="613ac-405">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="613ac-405">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="613ac-406">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="613ac-406">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="613ac-407">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="613ac-407">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="613ac-408">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="613ac-408">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="613ac-409">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="613ac-409">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="613ac-410">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="613ac-410">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="613ac-411">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="613ac-411">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="613ac-412">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="613ac-412">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="613ac-413">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="613ac-413">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="613ac-414">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="613ac-414">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="613ac-415">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="613ac-415">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="613ac-416">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="613ac-416">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="613ac-417">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="613ac-417">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="613ac-418">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="613ac-418">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="613ac-419">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="613ac-419">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="613ac-420">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="613ac-420">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="613ac-421">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="613ac-421">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="613ac-422">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="613ac-422">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="613ac-423">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="613ac-423">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="613ac-424">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="613ac-424">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="613ac-425">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="613ac-425">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="613ac-426">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="613ac-426">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="613ac-427">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="613ac-427">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="613ac-428">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="613ac-428">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="613ac-429">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="613ac-429">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="613ac-430">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="613ac-430">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="613ac-431">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="613ac-431">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="613ac-432">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="613ac-432">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="613ac-433">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="613ac-433">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="613ac-434">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="613ac-434">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="613ac-435">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="613ac-435">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="613ac-436">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="613ac-436">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="613ac-437">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="613ac-437">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="613ac-438">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="613ac-438">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="613ac-439">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="613ac-439">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="613ac-440">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="613ac-440">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="613ac-441">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="613ac-441">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="613ac-442">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="613ac-442">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="613ac-443">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="613ac-443">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="613ac-444">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="613ac-444">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="613ac-445">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="613ac-445">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="613ac-446">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="613ac-446">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="613ac-447">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="613ac-447">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="613ac-448">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="613ac-448">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-449">**État**</span><span class="sxs-lookup"><span data-stu-id="613ac-449">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-450">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-452">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="613ac-452">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-453">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="613ac-453">Current status of the object.</span></span> <span data-ttu-id="613ac-454">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="613ac-455">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="613ac-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="613ac-456">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="613ac-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="613ac-457">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="613ac-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="613ac-458">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="613ac-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="613ac-459">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="613ac-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="613ac-460">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="613ac-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="613ac-461">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="613ac-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="613ac-462">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="613ac-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="613ac-463">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="613ac-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="613ac-464">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="613ac-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="613ac-465">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="613ac-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="613ac-466">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="613ac-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="613ac-467">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="613ac-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="613ac-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-469">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="613ac-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-471">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="613ac-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="613ac-472">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="613ac-472">State of the logical device.</span></span> <span data-ttu-id="613ac-473">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="613ac-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="613ac-474">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="613ac-475">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="613ac-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="613ac-476">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="613ac-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="613ac-477">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="613ac-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="613ac-478">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="613ac-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="613ac-479">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="613ac-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="613ac-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="613ac-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-483">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="613ac-483">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="613ac-484">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="613ac-484">Scoping system's creation class name.</span></span>

<span data-ttu-id="613ac-485">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="613ac-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ac-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613ac-489">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="613ac-489">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="613ac-490">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="613ac-490">Scoping system's name.</span></span>

<span data-ttu-id="613ac-491">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="613ac-492">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="613ac-492">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613ac-493">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="613ac-493">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="613ac-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="613ac-494">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="613ac-495">Date et heure de la dernière réinitialisation du contrôleur, ce qui signifie que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="613ac-495">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="613ac-496">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-496">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="613ac-497">Notes</span><span class="sxs-lookup"><span data-stu-id="613ac-497">Remarks</span></span>

<span data-ttu-id="613ac-498">La classe **CIM \_ SerialController** est dérivée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-498">The **CIM\_SerialController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="613ac-499">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="613ac-499">WMI does not implement this class.</span></span> <span data-ttu-id="613ac-500">Pour les classes WMI dérivées de **CIM \_ SerialController**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="613ac-500">For WMI classes derived from **CIM\_SerialController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="613ac-501">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="613ac-501">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="613ac-502">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="613ac-502">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="613ac-503">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="613ac-503">Requirements</span></span>



| <span data-ttu-id="613ac-504">Condition requise</span><span class="sxs-lookup"><span data-stu-id="613ac-504">Requirement</span></span> | <span data-ttu-id="613ac-505">Valeur</span><span class="sxs-lookup"><span data-stu-id="613ac-505">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="613ac-506">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="613ac-506">Minimum supported client</span></span><br/> | <span data-ttu-id="613ac-507">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="613ac-507">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="613ac-508">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="613ac-508">Minimum supported server</span></span><br/> | <span data-ttu-id="613ac-509">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="613ac-509">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="613ac-510">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="613ac-510">Namespace</span></span><br/>                | <span data-ttu-id="613ac-511">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="613ac-511">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="613ac-512">MOF</span><span class="sxs-lookup"><span data-stu-id="613ac-512">MOF</span></span><br/>                      | <dl> <span data-ttu-id="613ac-513"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="613ac-513"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="613ac-514">DLL</span><span class="sxs-lookup"><span data-stu-id="613ac-514">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613ac-515"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613ac-515"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613ac-516">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="613ac-516">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613ac-517">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="613ac-517">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

