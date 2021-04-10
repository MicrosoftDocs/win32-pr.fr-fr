---
description: La \_ classe de contrôleur CIM est une classe parente permettant de regrouper divers appareils liés au contrôle. Les contrôleurs SCSI, les contrôleurs USB et les contrôleurs série sont des exemples de contrôleurs.
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: CIM_Controller, classe (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200964"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="13d15-104">CIM_Controller, classe (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="13d15-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="13d15-105">La classe de **\_ contrôleur CIM** est une classe parente permettant de regrouper divers appareils liés au contrôle.</span><span class="sxs-lookup"><span data-stu-id="13d15-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="13d15-106">Les contrôleurs SCSI, les contrôleurs USB et les contrôleurs série sont des exemples de contrôleurs.</span><span class="sxs-lookup"><span data-stu-id="13d15-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="13d15-107">La classe de **\_ contrôleur CIM** est une abstraction pour les appareils avec une pile de protocole unique, qui existe principalement pour la communication et le contrôle ou la réinitialisation des appareils en aval ([**CIM \_ ControlledBy**](cim-controlledby.md)).</span><span class="sxs-lookup"><span data-stu-id="13d15-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13d15-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="13d15-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="13d15-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="13d15-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="13d15-110">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="13d15-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13d15-111">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="13d15-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d15-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13d15-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="13d15-113">Membres</span><span class="sxs-lookup"><span data-stu-id="13d15-113">Members</span></span>

<span data-ttu-id="13d15-114">La classe de **\_ contrôleur CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="13d15-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="13d15-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="13d15-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="13d15-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13d15-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13d15-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="13d15-117">Methods</span></span>

<span data-ttu-id="13d15-118">La classe de **\_ contrôleur CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="13d15-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="13d15-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="13d15-119">Method</span></span>                                                                | <span data-ttu-id="13d15-120">Description</span><span class="sxs-lookup"><span data-stu-id="13d15-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13d15-121">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="13d15-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="13d15-122">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="13d15-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="13d15-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="13d15-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="13d15-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="13d15-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="13d15-125">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="13d15-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="13d15-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="13d15-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="13d15-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13d15-127">Properties</span></span>

<span data-ttu-id="13d15-128">La classe de **\_ contrôleur CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="13d15-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13d15-129">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="13d15-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-130">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d15-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="13d15-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-133">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="13d15-133">Availability and status of the device.</span></span>

<span data-ttu-id="13d15-134">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13d15-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="13d15-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13d15-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="13d15-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="13d15-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="13d15-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="13d15-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="13d15-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="13d15-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="13d15-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="13d15-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="13d15-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="13d15-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="13d15-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="13d15-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="13d15-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="13d15-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="13d15-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13d15-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="13d15-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="13d15-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="13d15-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="13d15-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="13d15-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="13d15-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="13d15-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-148">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="13d15-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="13d15-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="13d15-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-150">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="13d15-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="13d15-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="13d15-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-152">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="13d15-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="13d15-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="13d15-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="13d15-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="13d15-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-155">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="13d15-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="13d15-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="13d15-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-157">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="13d15-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="13d15-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="13d15-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-159">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="13d15-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="13d15-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="13d15-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-161">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="13d15-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="13d15-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="13d15-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-163">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="13d15-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13d15-164">**Caption**</span><span class="sxs-lookup"><span data-stu-id="13d15-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-167">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="13d15-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-168">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13d15-168">A short textual description of the object.</span></span>

<span data-ttu-id="13d15-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="13d15-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d15-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-173">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="13d15-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-174">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="13d15-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="13d15-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="13d15-176">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="13d15-176">**This device is working properly.**</span></span> <span data-ttu-id="13d15-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="13d15-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="13d15-178">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="13d15-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="13d15-179">(1)</span><span class="sxs-lookup"><span data-stu-id="13d15-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="13d15-180">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="13d15-181">(2)</span><span class="sxs-lookup"><span data-stu-id="13d15-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="13d15-182">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="13d15-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="13d15-183">(3)</span><span class="sxs-lookup"><span data-stu-id="13d15-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="13d15-184">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="13d15-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="13d15-185">(4)</span><span class="sxs-lookup"><span data-stu-id="13d15-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="13d15-186">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="13d15-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="13d15-187">(5)</span><span class="sxs-lookup"><span data-stu-id="13d15-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="13d15-188">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="13d15-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="13d15-189"> (6)</span><span class="sxs-lookup"><span data-stu-id="13d15-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="13d15-190">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="13d15-190">**Cannot filter.**</span></span> <span data-ttu-id="13d15-191">(7)</span><span class="sxs-lookup"><span data-stu-id="13d15-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="13d15-192">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="13d15-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="13d15-193">(8)</span><span class="sxs-lookup"><span data-stu-id="13d15-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="13d15-194">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="13d15-195">(9)</span><span class="sxs-lookup"><span data-stu-id="13d15-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="13d15-196">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-196">**This device cannot start.**</span></span> <span data-ttu-id="13d15-197">(10)</span><span class="sxs-lookup"><span data-stu-id="13d15-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="13d15-198">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-198">**This device failed.**</span></span> <span data-ttu-id="13d15-199">(11)</span><span class="sxs-lookup"><span data-stu-id="13d15-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="13d15-200">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="13d15-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="13d15-201">douze</span><span class="sxs-lookup"><span data-stu-id="13d15-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="13d15-202">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="13d15-203">(13)</span><span class="sxs-lookup"><span data-stu-id="13d15-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="13d15-204">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="13d15-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="13d15-205">(14)</span><span class="sxs-lookup"><span data-stu-id="13d15-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="13d15-206">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="13d15-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="13d15-207">(15)</span><span class="sxs-lookup"><span data-stu-id="13d15-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="13d15-208">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="13d15-209">(16)</span><span class="sxs-lookup"><span data-stu-id="13d15-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="13d15-210">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="13d15-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="13d15-211">(17)</span><span class="sxs-lookup"><span data-stu-id="13d15-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="13d15-212">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="13d15-213">(18)</span><span class="sxs-lookup"><span data-stu-id="13d15-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="13d15-214">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="13d15-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="13d15-215">(19)</span><span class="sxs-lookup"><span data-stu-id="13d15-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="13d15-216">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="13d15-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="13d15-217">(20)</span><span class="sxs-lookup"><span data-stu-id="13d15-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="13d15-218">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="13d15-219">(21)</span><span class="sxs-lookup"><span data-stu-id="13d15-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="13d15-220">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="13d15-220">**This device is disabled.**</span></span> <span data-ttu-id="13d15-221">(22)</span><span class="sxs-lookup"><span data-stu-id="13d15-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="13d15-222">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="13d15-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="13d15-223">(23)</span><span class="sxs-lookup"><span data-stu-id="13d15-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="13d15-224">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="13d15-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="13d15-225">(24)</span><span class="sxs-lookup"><span data-stu-id="13d15-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="13d15-226">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="13d15-227">(25)</span><span class="sxs-lookup"><span data-stu-id="13d15-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="13d15-228">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="13d15-229">(26)</span><span class="sxs-lookup"><span data-stu-id="13d15-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="13d15-230">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="13d15-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="13d15-231">(27)</span><span class="sxs-lookup"><span data-stu-id="13d15-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="13d15-232">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="13d15-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="13d15-233">(28)</span><span class="sxs-lookup"><span data-stu-id="13d15-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="13d15-234">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="13d15-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="13d15-235">(29)</span><span class="sxs-lookup"><span data-stu-id="13d15-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="13d15-236">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="13d15-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="13d15-237">(30)</span><span class="sxs-lookup"><span data-stu-id="13d15-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="13d15-238">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="13d15-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="13d15-239">31</span><span class="sxs-lookup"><span data-stu-id="13d15-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13d15-240">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="13d15-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-241">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13d15-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-243">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="13d15-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-244">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13d15-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="13d15-245">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-246">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13d15-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-249">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="13d15-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="13d15-250">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="13d15-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="13d15-251">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="13d15-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="13d15-252">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-253">**Description**</span><span class="sxs-lookup"><span data-stu-id="13d15-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-256">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="13d15-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-257">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13d15-257">A textual description of the object.</span></span>

<span data-ttu-id="13d15-258">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-259">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="13d15-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-262">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="13d15-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="13d15-263">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="13d15-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="13d15-264">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-265">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="13d15-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-266">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13d15-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d15-268">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="13d15-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="13d15-269">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="13d15-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d15-273">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="13d15-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="13d15-274">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="13d15-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-276">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13d15-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-278">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="13d15-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-279">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="13d15-279">Indicates when the object was installed.</span></span> <span data-ttu-id="13d15-280">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="13d15-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="13d15-281">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-282">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="13d15-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d15-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d15-285">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="13d15-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="13d15-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="13d15-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-288">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d15-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-290">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="13d15-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-291">Nombre maximal d’entités directement adressables prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="13d15-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="13d15-292">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="13d15-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="13d15-293">**Nom**</span><span class="sxs-lookup"><span data-stu-id="13d15-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-296">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="13d15-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-297">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="13d15-297">Label by which the object is known.</span></span> <span data-ttu-id="13d15-298">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="13d15-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="13d15-299">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="13d15-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-303">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="13d15-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-304">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="13d15-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="13d15-305">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="13d15-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="13d15-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-307">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="13d15-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-308">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d15-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13d15-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d15-310">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="13d15-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="13d15-311">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13d15-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="13d15-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-313">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="13d15-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="13d15-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="13d15-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-315">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="13d15-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="13d15-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="13d15-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-317">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="13d15-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="13d15-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="13d15-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-319">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="13d15-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="13d15-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="13d15-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-321">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="13d15-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="13d15-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="13d15-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-323">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="13d15-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="13d15-324">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="13d15-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="13d15-325">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="13d15-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="13d15-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="13d15-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-327">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="13d15-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="13d15-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="13d15-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="13d15-329">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="13d15-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="13d15-330">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="13d15-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-331">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="13d15-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d15-333">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="13d15-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="13d15-334">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="13d15-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="13d15-335">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="13d15-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="13d15-336">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="13d15-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="13d15-337">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-338">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="13d15-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-339">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d15-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-341">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="13d15-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-342">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="13d15-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13d15-343">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="13d15-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13d15-344">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="13d15-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="13d15-345">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="13d15-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="13d15-346">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="13d15-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="13d15-347">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="13d15-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="13d15-348">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="13d15-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="13d15-349">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="13d15-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="13d15-350">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="13d15-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="13d15-351">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="13d15-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="13d15-352">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="13d15-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="13d15-353">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="13d15-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="13d15-354">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="13d15-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="13d15-355">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="13d15-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="13d15-356">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="13d15-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="13d15-357">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="13d15-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="13d15-358">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="13d15-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="13d15-359">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="13d15-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="13d15-360">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="13d15-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="13d15-361">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="13d15-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="13d15-362">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="13d15-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="13d15-363">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="13d15-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="13d15-364">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="13d15-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="13d15-365">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="13d15-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="13d15-366">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="13d15-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="13d15-367">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="13d15-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="13d15-368">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="13d15-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="13d15-369">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="13d15-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="13d15-370">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="13d15-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="13d15-371">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="13d15-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="13d15-372">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="13d15-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="13d15-373">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="13d15-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="13d15-374">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="13d15-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="13d15-375">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="13d15-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="13d15-376">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="13d15-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="13d15-377">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="13d15-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="13d15-378">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="13d15-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="13d15-379">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="13d15-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="13d15-380">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="13d15-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="13d15-381">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="13d15-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="13d15-382">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="13d15-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="13d15-383">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="13d15-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="13d15-384">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="13d15-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="13d15-385">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="13d15-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="13d15-386">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="13d15-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="13d15-387">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="13d15-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="13d15-388">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="13d15-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="13d15-389">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="13d15-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13d15-390">**État**</span><span class="sxs-lookup"><span data-stu-id="13d15-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-393">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="13d15-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-394">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13d15-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="13d15-395">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="13d15-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="13d15-396">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="13d15-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="13d15-397">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="13d15-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="13d15-398">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="13d15-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="13d15-399">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="13d15-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="13d15-400">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="13d15-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="13d15-401">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="13d15-402">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="13d15-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="13d15-403">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="13d15-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="13d15-404">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="13d15-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="13d15-405">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="13d15-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13d15-406">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="13d15-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="13d15-407">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="13d15-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="13d15-408">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="13d15-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="13d15-409">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="13d15-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="13d15-410">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="13d15-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="13d15-411">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="13d15-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="13d15-412">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="13d15-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="13d15-413">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="13d15-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="13d15-414">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="13d15-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13d15-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="13d15-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-416">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13d15-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-418">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="13d15-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="13d15-419">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="13d15-419">State of the logical device.</span></span> <span data-ttu-id="13d15-420">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="13d15-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="13d15-421">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="13d15-422">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="13d15-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="13d15-423">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="13d15-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="13d15-424">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="13d15-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="13d15-425">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="13d15-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="13d15-426">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="13d15-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13d15-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="13d15-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-430">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="13d15-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="13d15-431">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="13d15-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="13d15-432">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="13d15-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13d15-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13d15-436">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="13d15-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="13d15-437">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="13d15-437">The scoping system's name.</span></span>

<span data-ttu-id="13d15-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="13d15-439">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="13d15-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13d15-440">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13d15-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13d15-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13d15-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13d15-442">Date et heure de la dernière réinitialisation du contrôleur (mise hors tension ou réinitialisée).</span><span class="sxs-lookup"><span data-stu-id="13d15-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13d15-443">Notes</span><span class="sxs-lookup"><span data-stu-id="13d15-443">Remarks</span></span>

<span data-ttu-id="13d15-444">La classe de **\_ contrôleur CIM** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="13d15-445">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="13d15-445">WMI does not implement this class.</span></span> <span data-ttu-id="13d15-446">Pour les classes dérivées du **\_ contrôleur CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="13d15-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="13d15-447">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="13d15-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="13d15-448">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="13d15-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d15-449">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13d15-449">Requirements</span></span>



| <span data-ttu-id="13d15-450">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13d15-450">Requirement</span></span> | <span data-ttu-id="13d15-451">Valeur</span><span class="sxs-lookup"><span data-stu-id="13d15-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d15-452">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13d15-452">Minimum supported client</span></span><br/> | <span data-ttu-id="13d15-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13d15-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="13d15-454">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13d15-454">Minimum supported server</span></span><br/> | <span data-ttu-id="13d15-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13d15-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="13d15-456">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13d15-456">Namespace</span></span><br/>                | <span data-ttu-id="13d15-457">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="13d15-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="13d15-458">MOF</span><span class="sxs-lookup"><span data-stu-id="13d15-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13d15-459"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13d15-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="13d15-460">DLL</span><span class="sxs-lookup"><span data-stu-id="13d15-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13d15-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13d15-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d15-462">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13d15-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d15-463">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="13d15-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

