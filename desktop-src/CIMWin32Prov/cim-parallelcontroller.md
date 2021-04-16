---
description: L' \_ Association CIM ParallelController se réfère aux fonctionnalités et à la gestion de l’unité logique de port parallèle.
ms.assetid: c05e79b6-f3a6-48cc-a831-b67e216f43eb
ms.tgt_platform: multiple
title: Classe CIM_ParallelController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParallelController
- CIM_ParallelController.Availability
- CIM_ParallelController.Capabilities
- CIM_ParallelController.CapabilityDescriptions
- CIM_ParallelController.Caption
- CIM_ParallelController.ConfigManagerErrorCode
- CIM_ParallelController.ConfigManagerUserConfig
- CIM_ParallelController.CreationClassName
- CIM_ParallelController.Description
- CIM_ParallelController.DeviceID
- CIM_ParallelController.DMASupport
- CIM_ParallelController.ErrorCleared
- CIM_ParallelController.ErrorDescription
- CIM_ParallelController.InstallDate
- CIM_ParallelController.LastErrorCode
- CIM_ParallelController.MaxNumberControlled
- CIM_ParallelController.Name
- CIM_ParallelController.PNPDeviceID
- CIM_ParallelController.PowerManagementCapabilities
- CIM_ParallelController.PowerManagementSupported
- CIM_ParallelController.ProtocolSupported
- CIM_ParallelController.Status
- CIM_ParallelController.StatusInfo
- CIM_ParallelController.SystemCreationClassName
- CIM_ParallelController.SystemName
- CIM_ParallelController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc21290de08b6e22c0bc69ec127f3c996ee5b65e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524023"
---
# <a name="cim_parallelcontroller-class"></a><span data-ttu-id="d83b9-103">\_Classe CIM ParallelController</span><span class="sxs-lookup"><span data-stu-id="d83b9-103">CIM\_ParallelController class</span></span>

<span data-ttu-id="d83b9-104">L’Association **CIM \_ ParallelController** se réfère aux fonctionnalités et à la gestion de l’unité logique de port parallèle.</span><span class="sxs-lookup"><span data-stu-id="d83b9-104">The **CIM\_ParallelController** association relates to the capabilities and management of the parallel port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d83b9-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d83b9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d83b9-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d83b9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d83b9-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d83b9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d83b9-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="d83b9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d83b9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d83b9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C552-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ParallelController : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="d83b9-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d83b9-110">Members</span></span>

<span data-ttu-id="d83b9-111">La classe **CIM \_ ParallelController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d83b9-111">The **CIM\_ParallelController** class has these types of members:</span></span>

-   [<span data-ttu-id="d83b9-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d83b9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d83b9-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d83b9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d83b9-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d83b9-114">Methods</span></span>

<span data-ttu-id="d83b9-115">La classe **CIM \_ ParallelController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d83b9-115">The **CIM\_ParallelController** class has these methods.</span></span>



| <span data-ttu-id="d83b9-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="d83b9-116">Method</span></span>                                                                        | <span data-ttu-id="d83b9-117">Description</span><span class="sxs-lookup"><span data-stu-id="d83b9-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d83b9-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="d83b9-118">**Reset**</span></span>](reset-method-in-class-cim-parallelcontroller.md)                 | <span data-ttu-id="d83b9-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d83b9-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="d83b9-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d83b9-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="d83b9-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d83b9-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-parallelcontroller.md) | <span data-ttu-id="d83b9-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="d83b9-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d83b9-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="d83b9-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d83b9-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d83b9-124">Properties</span></span>

<span data-ttu-id="d83b9-125">La classe **CIM \_ ParallelController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d83b9-125">The **CIM\_ParallelController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d83b9-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="d83b9-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d83b9-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d83b9-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-130">Availability and status of the device.</span></span>

<span data-ttu-id="d83b9-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d83b9-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d83b9-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d83b9-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d83b9-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d83b9-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="d83b9-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d83b9-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="d83b9-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d83b9-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="d83b9-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d83b9-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d83b9-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d83b9-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="d83b9-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d83b9-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="d83b9-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d83b9-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="d83b9-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d83b9-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="d83b9-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d83b9-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="d83b9-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d83b9-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="d83b9-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d83b9-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="d83b9-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-145">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="d83b9-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d83b9-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="d83b9-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-147">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="d83b9-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d83b9-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="d83b9-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-149">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="d83b9-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d83b9-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="d83b9-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d83b9-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="d83b9-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-152">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d83b9-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d83b9-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="d83b9-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-154">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="d83b9-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d83b9-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="d83b9-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-156">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="d83b9-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d83b9-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="d83b9-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-158">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="d83b9-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d83b9-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="d83b9-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-160">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="d83b9-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d83b9-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-162">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d83b9-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-164">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ports parallèles DMTF \| 003,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="d83b9-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-165">Fonctionnalités du contrôleur parallèle.</span><span class="sxs-lookup"><span data-stu-id="d83b9-165">Capabilities of the parallel controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d83b9-166">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d83b9-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d83b9-167">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d83b9-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="d83b9-168">**Compatible XT/AT** (2)</span><span class="sxs-lookup"><span data-stu-id="d83b9-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="d83b9-169">**Compatible PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="d83b9-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="d83b9-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="d83b9-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="d83b9-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="d83b9-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="d83b9-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="d83b9-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="d83b9-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="d83b9-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="d83b9-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="d83b9-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d83b9-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-176">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d83b9-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-178">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ParallelController**.**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="d83b9-178">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-179">Chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités du contrôleur parallèle indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="d83b9-179">Free-form strings that provide detailed explanations for the parallel controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="d83b9-180">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** , qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="d83b9-180">Each entry of this array is related to the entry in the **Capabilities** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="d83b9-181">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d83b9-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-184">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-185">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d83b9-185">Short textual description of the object.</span></span>

<span data-ttu-id="d83b9-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d83b9-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-188">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d83b9-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-190">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d83b9-190">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-191">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="d83b9-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d83b9-192">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d83b9-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d83b9-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="d83b9-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-195">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="d83b9-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d83b9-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d83b9-197">(1)</span><span class="sxs-lookup"><span data-stu-id="d83b9-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-198">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="d83b9-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d83b9-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d83b9-200">(2)</span><span class="sxs-lookup"><span data-stu-id="d83b9-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d83b9-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d83b9-202">(3)</span><span class="sxs-lookup"><span data-stu-id="d83b9-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-203">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="d83b9-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d83b9-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d83b9-205">(4)</span><span class="sxs-lookup"><span data-stu-id="d83b9-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-206">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="d83b9-206">Device is not working properly.</span></span> <span data-ttu-id="d83b9-207">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="d83b9-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d83b9-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d83b9-209">(5)</span><span class="sxs-lookup"><span data-stu-id="d83b9-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-210">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="d83b9-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d83b9-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d83b9-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="d83b9-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-213">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="d83b9-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d83b9-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d83b9-215">(7)</span><span class="sxs-lookup"><span data-stu-id="d83b9-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d83b9-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d83b9-217">(8)</span><span class="sxs-lookup"><span data-stu-id="d83b9-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-218">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="d83b9-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d83b9-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d83b9-220">(9)</span><span class="sxs-lookup"><span data-stu-id="d83b9-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-221">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-221">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d83b9-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d83b9-223">(10)</span><span class="sxs-lookup"><span data-stu-id="d83b9-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-224">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d83b9-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d83b9-226">(11)</span><span class="sxs-lookup"><span data-stu-id="d83b9-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-227">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d83b9-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d83b9-229">douze</span><span class="sxs-lookup"><span data-stu-id="d83b9-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-230">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d83b9-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d83b9-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d83b9-232">(13)</span><span class="sxs-lookup"><span data-stu-id="d83b9-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-233">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d83b9-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d83b9-235">(14)</span><span class="sxs-lookup"><span data-stu-id="d83b9-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-236">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="d83b9-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d83b9-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d83b9-238">(15)</span><span class="sxs-lookup"><span data-stu-id="d83b9-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-239">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="d83b9-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d83b9-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d83b9-241">(16)</span><span class="sxs-lookup"><span data-stu-id="d83b9-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-242">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d83b9-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d83b9-244">(17)</span><span class="sxs-lookup"><span data-stu-id="d83b9-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-245">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="d83b9-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d83b9-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d83b9-247">(18)</span><span class="sxs-lookup"><span data-stu-id="d83b9-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-248">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="d83b9-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d83b9-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d83b9-250">(19)</span><span class="sxs-lookup"><span data-stu-id="d83b9-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d83b9-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d83b9-252">(20)</span><span class="sxs-lookup"><span data-stu-id="d83b9-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-253">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="d83b9-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d83b9-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d83b9-255">(21)</span><span class="sxs-lookup"><span data-stu-id="d83b9-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-256">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="d83b9-256">System failure.</span></span> <span data-ttu-id="d83b9-257">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="d83b9-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d83b9-258">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d83b9-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d83b9-260">(22)</span><span class="sxs-lookup"><span data-stu-id="d83b9-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-261">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d83b9-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d83b9-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d83b9-263">(23)</span><span class="sxs-lookup"><span data-stu-id="d83b9-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-264">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="d83b9-264">System failure.</span></span> <span data-ttu-id="d83b9-265">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="d83b9-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d83b9-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d83b9-267">(24)</span><span class="sxs-lookup"><span data-stu-id="d83b9-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-268">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="d83b9-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d83b9-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d83b9-270">(25)</span><span class="sxs-lookup"><span data-stu-id="d83b9-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-271">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d83b9-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d83b9-273">(26)</span><span class="sxs-lookup"><span data-stu-id="d83b9-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-274">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d83b9-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d83b9-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d83b9-276">(27)</span><span class="sxs-lookup"><span data-stu-id="d83b9-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-277">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="d83b9-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d83b9-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d83b9-279">(28)</span><span class="sxs-lookup"><span data-stu-id="d83b9-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-280">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="d83b9-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d83b9-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d83b9-282">(29)</span><span class="sxs-lookup"><span data-stu-id="d83b9-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-283">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="d83b9-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d83b9-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d83b9-285">(30)</span><span class="sxs-lookup"><span data-stu-id="d83b9-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-286">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="d83b9-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d83b9-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="d83b9-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d83b9-288">31</span><span class="sxs-lookup"><span data-stu-id="d83b9-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-289">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="d83b9-289">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d83b9-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-291">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d83b9-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-293">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d83b9-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-294">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d83b9-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d83b9-295">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d83b9-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-299">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d83b9-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-300">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d83b9-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d83b9-301">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="d83b9-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d83b9-302">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-303">**Description**</span><span class="sxs-lookup"><span data-stu-id="d83b9-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-306">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d83b9-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-307">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d83b9-307">Textual description of the object.</span></span>

<span data-ttu-id="d83b9-308">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d83b9-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-312">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d83b9-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-313">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d83b9-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d83b9-314">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-315">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="d83b9-315">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-316">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d83b9-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-318">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Ports parallèles DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="d83b9-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-319">Si la **valeur est true**, l’accès direct à la mémoire (DMA) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d83b9-319">If **TRUE**, direct memory access (DMA) is supported.</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d83b9-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-321">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d83b9-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-323">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="d83b9-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d83b9-324">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d83b9-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-328">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="d83b9-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d83b9-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d83b9-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-331">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d83b9-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-333">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="d83b9-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-334">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d83b9-334">Date and time the object was installed.</span></span> <span data-ttu-id="d83b9-335">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="d83b9-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d83b9-336">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d83b9-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-338">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d83b9-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-340">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d83b9-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d83b9-341">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-342">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="d83b9-342">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-343">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d83b9-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-345">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="d83b9-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-346">Nombre maximal d’entités directement adressables prises en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="d83b9-346">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="d83b9-347">La valeur 0 (zéro) doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="d83b9-347">A value of 0 (zero) should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="d83b9-348">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-348">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-349">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d83b9-349">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-352">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d83b9-352">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-353">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d83b9-353">Label by which the object is known.</span></span> <span data-ttu-id="d83b9-354">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="d83b9-354">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d83b9-355">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-355">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-356">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d83b9-356">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-357">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-359">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d83b9-359">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-360">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="d83b9-360">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="d83b9-361">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d83b9-362">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="d83b9-362">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d83b9-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-364">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d83b9-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-366">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="d83b9-366">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d83b9-367">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="d83b9-367">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d83b9-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d83b9-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d83b9-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="d83b9-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d83b9-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="d83b9-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d83b9-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="d83b9-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-372">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="d83b9-372">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d83b9-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="d83b9-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-374">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="d83b9-374">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d83b9-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="d83b9-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-376">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d83b9-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d83b9-377">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="d83b9-377">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d83b9-378">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d83b9-378">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d83b9-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="d83b9-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-380">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="d83b9-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d83b9-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="d83b9-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d83b9-382">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="d83b9-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-383">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d83b9-383">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-384">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d83b9-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-386">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="d83b9-386">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d83b9-387">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d83b9-387">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d83b9-388">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d83b9-388">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d83b9-389">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d83b9-389">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="d83b9-390">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-391">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="d83b9-391">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-392">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d83b9-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-394">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d83b9-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-395">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="d83b9-395">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="d83b9-396">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-396">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="d83b9-397">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d83b9-397">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d83b9-398">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d83b9-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d83b9-399">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d83b9-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="d83b9-400">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="d83b9-400">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="d83b9-401">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="d83b9-401">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="d83b9-402">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="d83b9-402">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="d83b9-403">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="d83b9-403">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="d83b9-404">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="d83b9-404">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="d83b9-405">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="d83b9-405">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="d83b9-406">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="d83b9-406">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="d83b9-407">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="d83b9-407">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="d83b9-408">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="d83b9-408">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="d83b9-409">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="d83b9-409">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="d83b9-410">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="d83b9-410">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="d83b9-411">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="d83b9-411">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="d83b9-412">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="d83b9-412">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="d83b9-413">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="d83b9-413">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="d83b9-414">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="d83b9-414">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="d83b9-415">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="d83b9-415">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d83b9-416">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="d83b9-416">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="d83b9-417">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="d83b9-417">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="d83b9-418">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="d83b9-418">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="d83b9-419">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="d83b9-419">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="d83b9-420">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="d83b9-420">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="d83b9-421">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="d83b9-421">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="d83b9-422">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="d83b9-422">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="d83b9-423">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="d83b9-423">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="d83b9-424">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="d83b9-424">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="d83b9-425">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="d83b9-425">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="d83b9-426">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="d83b9-426">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="d83b9-427">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="d83b9-427">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="d83b9-428">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="d83b9-428">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="d83b9-429">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="d83b9-429">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="d83b9-430">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="d83b9-430">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="d83b9-431">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="d83b9-431">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="d83b9-432">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="d83b9-432">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="d83b9-433">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="d83b9-433">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="d83b9-434">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="d83b9-434">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="d83b9-435">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="d83b9-435">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="d83b9-436">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="d83b9-436">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="d83b9-437">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="d83b9-437">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="d83b9-438">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="d83b9-438">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="d83b9-439">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="d83b9-439">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="d83b9-440">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="d83b9-440">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="d83b9-441">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="d83b9-441">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="d83b9-442">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="d83b9-442">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="d83b9-443">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="d83b9-443">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="d83b9-444">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="d83b9-444">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-445">**État**</span><span class="sxs-lookup"><span data-stu-id="d83b9-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-446">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-448">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d83b9-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-449">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d83b9-449">Current status of the object.</span></span> <span data-ttu-id="d83b9-450">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d83b9-451">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d83b9-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d83b9-452">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d83b9-453">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d83b9-454">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d83b9-455">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="d83b9-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d83b9-456">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d83b9-457">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d83b9-458">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d83b9-459">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d83b9-460">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d83b9-461">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d83b9-462">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d83b9-463">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="d83b9-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d83b9-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-465">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d83b9-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-467">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d83b9-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-468">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d83b9-468">State of the logical device.</span></span> <span data-ttu-id="d83b9-469">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d83b9-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d83b9-470">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d83b9-471">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="d83b9-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d83b9-472">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="d83b9-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d83b9-473">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="d83b9-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d83b9-474">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="d83b9-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d83b9-475">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d83b9-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d83b9-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d83b9-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-477">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-478">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-479">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d83b9-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-480">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d83b9-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="d83b9-481">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d83b9-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-483">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d83b9-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-484">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-485">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d83b9-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-486">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d83b9-486">Scoping system's name.</span></span>

<span data-ttu-id="d83b9-487">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d83b9-488">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="d83b9-488">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83b9-489">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d83b9-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d83b9-490">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d83b9-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d83b9-491">Date et heure de la dernière réinitialisation du contrôleur, ce qui signifie que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="d83b9-491">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="d83b9-492">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-492">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d83b9-493">Notes</span><span class="sxs-lookup"><span data-stu-id="d83b9-493">Remarks</span></span>

<span data-ttu-id="d83b9-494">La classe **CIM \_ ParallelController** est dérivée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-494">The **CIM\_ParallelController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="d83b9-495">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="d83b9-495">WMI does not implement this class.</span></span> <span data-ttu-id="d83b9-496">Pour les classes WMI dérivées de **CIM \_ ParallelController**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d83b9-496">For WMI classes that are derived from **CIM\_ParallelController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d83b9-497">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d83b9-497">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d83b9-498">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d83b9-498">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d83b9-499">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d83b9-499">Requirements</span></span>



| <span data-ttu-id="d83b9-500">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d83b9-500">Requirement</span></span> | <span data-ttu-id="d83b9-501">Valeur</span><span class="sxs-lookup"><span data-stu-id="d83b9-501">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d83b9-502">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d83b9-502">Minimum supported client</span></span><br/> | <span data-ttu-id="d83b9-503">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d83b9-503">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d83b9-504">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d83b9-504">Minimum supported server</span></span><br/> | <span data-ttu-id="d83b9-505">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d83b9-505">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d83b9-506">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d83b9-506">Namespace</span></span><br/>                | <span data-ttu-id="d83b9-507">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d83b9-507">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d83b9-508">MOF</span><span class="sxs-lookup"><span data-stu-id="d83b9-508">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d83b9-509"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d83b9-509"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d83b9-510">DLL</span><span class="sxs-lookup"><span data-stu-id="d83b9-510">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d83b9-511"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d83b9-511"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d83b9-512">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d83b9-512">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d83b9-513">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="d83b9-513">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

