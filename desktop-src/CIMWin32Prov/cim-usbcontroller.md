---
description: La \_ classe CIM USBController représente les fonctionnalités et la gestion d’un contrôleur USB.
ms.assetid: fa891db5-9995-4532-895f-bded8dd0bdac
ms.tgt_platform: multiple
title: Classe CIM_USBController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBController
- CIM_USBController.Availability
- CIM_USBController.Caption
- CIM_USBController.ConfigManagerErrorCode
- CIM_USBController.ConfigManagerUserConfig
- CIM_USBController.CreationClassName
- CIM_USBController.Description
- CIM_USBController.DeviceID
- CIM_USBController.ErrorCleared
- CIM_USBController.ErrorDescription
- CIM_USBController.InstallDate
- CIM_USBController.LastErrorCode
- CIM_USBController.Manufacturer
- CIM_USBController.MaxNumberControlled
- CIM_USBController.Name
- CIM_USBController.PNPDeviceID
- CIM_USBController.PowerManagementCapabilities
- CIM_USBController.PowerManagementSupported
- CIM_USBController.ProtocolSupported
- CIM_USBController.Status
- CIM_USBController.StatusInfo
- CIM_USBController.SystemCreationClassName
- CIM_USBController.SystemName
- CIM_USBController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4c636ae977dc0145b9e4b243c6903a687a525d15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200865"
---
# <a name="cim_usbcontroller-class"></a><span data-ttu-id="029aa-103">\_Classe CIM USBController</span><span class="sxs-lookup"><span data-stu-id="029aa-103">CIM\_USBController class</span></span>

<span data-ttu-id="029aa-104">La classe **CIM \_ USBController** représente les fonctionnalités et la gestion d’un contrôleur USB.</span><span class="sxs-lookup"><span data-stu-id="029aa-104">The **CIM\_USBController** class represents the capabilities and management of a USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="029aa-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="029aa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="029aa-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="029aa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="029aa-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="029aa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="029aa-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="029aa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="029aa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="029aa-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_USBController : CIM_Controller
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
  uint32   LastErrorCode;
  string   Manufacturer;
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

## <a name="members"></a><span data-ttu-id="029aa-110">Membres</span><span class="sxs-lookup"><span data-stu-id="029aa-110">Members</span></span>

<span data-ttu-id="029aa-111">La classe **CIM \_ USBController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="029aa-111">The **CIM\_USBController** class has these types of members:</span></span>

-   [<span data-ttu-id="029aa-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="029aa-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="029aa-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="029aa-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="029aa-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="029aa-114">Methods</span></span>

<span data-ttu-id="029aa-115">La classe **CIM \_ USBController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="029aa-115">The **CIM\_USBController** class has these methods.</span></span>



| <span data-ttu-id="029aa-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="029aa-116">Method</span></span>                                                                   | <span data-ttu-id="029aa-117">Description</span><span class="sxs-lookup"><span data-stu-id="029aa-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="029aa-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="029aa-118">**Reset**</span></span>](reset-method-in-class-cim-usbcontroller.md)                 | <span data-ttu-id="029aa-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="029aa-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="029aa-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="029aa-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="029aa-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="029aa-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbcontroller.md) | <span data-ttu-id="029aa-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="029aa-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="029aa-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="029aa-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="029aa-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="029aa-124">Properties</span></span>

<span data-ttu-id="029aa-125">La classe **CIM \_ USBController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="029aa-125">The **CIM\_USBController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="029aa-126">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="029aa-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-127">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="029aa-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-129">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="029aa-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-130">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-130">Availability and status of the device.</span></span>

<span data-ttu-id="029aa-131">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="029aa-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="029aa-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="029aa-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="029aa-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="029aa-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="029aa-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-135">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="029aa-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="029aa-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="029aa-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="029aa-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="029aa-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="029aa-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="029aa-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="029aa-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="029aa-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="029aa-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="029aa-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="029aa-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="029aa-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="029aa-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="029aa-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="029aa-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="029aa-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="029aa-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="029aa-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="029aa-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="029aa-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-146">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="029aa-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="029aa-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="029aa-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-148">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="029aa-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="029aa-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="029aa-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-150">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="029aa-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="029aa-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="029aa-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="029aa-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="029aa-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-153">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="029aa-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="029aa-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="029aa-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-155">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="029aa-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="029aa-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="029aa-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-157">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="029aa-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="029aa-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="029aa-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-159">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="029aa-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="029aa-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="029aa-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-161">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="029aa-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="029aa-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="029aa-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-165">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="029aa-165">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-166">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="029aa-166">Short textual description of the object.</span></span>

<span data-ttu-id="029aa-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-168">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="029aa-168">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-169">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="029aa-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-171">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="029aa-171">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-172">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="029aa-172">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="029aa-173">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-173">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="029aa-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="029aa-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="029aa-175"> (0)</span><span class="sxs-lookup"><span data-stu-id="029aa-175">(0)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-176">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="029aa-176">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="029aa-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="029aa-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="029aa-178">(1)</span><span class="sxs-lookup"><span data-stu-id="029aa-178">(1)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-179">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="029aa-179">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="029aa-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="029aa-181">(2)</span><span class="sxs-lookup"><span data-stu-id="029aa-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="029aa-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="029aa-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="029aa-183">(3)</span><span class="sxs-lookup"><span data-stu-id="029aa-183">(3)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-184">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="029aa-184">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="029aa-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="029aa-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="029aa-186">(4)</span><span class="sxs-lookup"><span data-stu-id="029aa-186">(4)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-187">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="029aa-187">Device is not working properly.</span></span> <span data-ttu-id="029aa-188">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="029aa-188">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="029aa-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="029aa-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="029aa-190">(5)</span><span class="sxs-lookup"><span data-stu-id="029aa-190">(5)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-191">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="029aa-191">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="029aa-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="029aa-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="029aa-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="029aa-193">(6)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-194">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="029aa-194">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="029aa-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="029aa-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="029aa-196">(7)</span><span class="sxs-lookup"><span data-stu-id="029aa-196">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="029aa-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="029aa-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="029aa-198">(8)</span><span class="sxs-lookup"><span data-stu-id="029aa-198">(8)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-199">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="029aa-199">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="029aa-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="029aa-201">(9)</span><span class="sxs-lookup"><span data-stu-id="029aa-201">(9)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-202">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="029aa-202">Device is not working properly.</span></span> <span data-ttu-id="029aa-203">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-203">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="029aa-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="029aa-205">(10)</span><span class="sxs-lookup"><span data-stu-id="029aa-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-206">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="029aa-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="029aa-208">(11)</span><span class="sxs-lookup"><span data-stu-id="029aa-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-209">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="029aa-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="029aa-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="029aa-211">douze</span><span class="sxs-lookup"><span data-stu-id="029aa-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-212">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="029aa-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="029aa-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="029aa-214">(13)</span><span class="sxs-lookup"><span data-stu-id="029aa-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-215">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="029aa-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="029aa-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="029aa-217">(14)</span><span class="sxs-lookup"><span data-stu-id="029aa-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-218">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="029aa-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="029aa-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="029aa-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="029aa-220">(15)</span><span class="sxs-lookup"><span data-stu-id="029aa-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-221">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="029aa-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="029aa-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="029aa-223">(16)</span><span class="sxs-lookup"><span data-stu-id="029aa-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-224">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="029aa-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="029aa-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="029aa-226">(17)</span><span class="sxs-lookup"><span data-stu-id="029aa-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-227">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="029aa-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="029aa-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="029aa-229">(18)</span><span class="sxs-lookup"><span data-stu-id="029aa-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-230">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="029aa-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="029aa-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="029aa-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="029aa-232">(19)</span><span class="sxs-lookup"><span data-stu-id="029aa-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="029aa-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="029aa-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="029aa-234">(20)</span><span class="sxs-lookup"><span data-stu-id="029aa-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-235">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="029aa-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="029aa-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="029aa-237">(21)</span><span class="sxs-lookup"><span data-stu-id="029aa-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-238">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="029aa-238">System failure.</span></span> <span data-ttu-id="029aa-239">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="029aa-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="029aa-240">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="029aa-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="029aa-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="029aa-242">(22)</span><span class="sxs-lookup"><span data-stu-id="029aa-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-243">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="029aa-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="029aa-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="029aa-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="029aa-245">(23)</span><span class="sxs-lookup"><span data-stu-id="029aa-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-246">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="029aa-246">System failure.</span></span> <span data-ttu-id="029aa-247">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="029aa-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="029aa-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="029aa-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="029aa-249">(24)</span><span class="sxs-lookup"><span data-stu-id="029aa-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-250">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="029aa-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="029aa-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="029aa-252">(25)</span><span class="sxs-lookup"><span data-stu-id="029aa-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-253">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="029aa-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="029aa-255">(26)</span><span class="sxs-lookup"><span data-stu-id="029aa-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-256">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="029aa-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="029aa-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="029aa-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="029aa-258">(27)</span><span class="sxs-lookup"><span data-stu-id="029aa-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-259">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="029aa-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="029aa-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="029aa-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="029aa-261">(28)</span><span class="sxs-lookup"><span data-stu-id="029aa-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-262">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="029aa-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="029aa-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="029aa-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="029aa-264">(29)</span><span class="sxs-lookup"><span data-stu-id="029aa-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-265">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="029aa-265">Device is disabled.</span></span> <span data-ttu-id="029aa-266">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="029aa-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="029aa-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="029aa-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="029aa-268">(30)</span><span class="sxs-lookup"><span data-stu-id="029aa-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-269">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="029aa-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="029aa-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="029aa-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="029aa-271">31</span><span class="sxs-lookup"><span data-stu-id="029aa-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-272">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="029aa-272">Device is not working properly.</span></span> <span data-ttu-id="029aa-273">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="029aa-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="029aa-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="029aa-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-275">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="029aa-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-277">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="029aa-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-278">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="029aa-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="029aa-279">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-280">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="029aa-280">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-283">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="029aa-283">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="029aa-284">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="029aa-284">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="029aa-285">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="029aa-285">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="029aa-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-287">**Description**</span><span class="sxs-lookup"><span data-stu-id="029aa-287">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-290">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="029aa-290">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-291">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="029aa-291">Textual description of the object.</span></span>

<span data-ttu-id="029aa-292">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-292">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-293">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="029aa-293">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-296">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="029aa-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="029aa-297">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="029aa-297">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="029aa-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-299">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="029aa-299">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-300">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="029aa-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="029aa-302">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="029aa-302">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="029aa-303">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-304">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="029aa-304">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="029aa-307">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="029aa-307">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="029aa-308">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-309">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="029aa-309">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-310">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="029aa-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-312">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="029aa-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-313">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="029aa-313">Date and time the object was installed.</span></span> <span data-ttu-id="029aa-314">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="029aa-314">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="029aa-315">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-315">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="029aa-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-317">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="029aa-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="029aa-319">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="029aa-319">Last error code reported by the logical device.</span></span>

<span data-ttu-id="029aa-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-321">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="029aa-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-324">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="029aa-324">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-325">Nom du fabricant du contrôleur USB.</span><span class="sxs-lookup"><span data-stu-id="029aa-325">Name of the USB controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="029aa-326">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="029aa-326">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-327">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="029aa-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-329">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="029aa-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-330">Nombre maximal d’entités directement adressables prises en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="029aa-330">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="029aa-331">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="029aa-331">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="029aa-332">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-332">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-333">**Nom**</span><span class="sxs-lookup"><span data-stu-id="029aa-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-336">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="029aa-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-337">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="029aa-337">Label by which the object is known.</span></span> <span data-ttu-id="029aa-338">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="029aa-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="029aa-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="029aa-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-343">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="029aa-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-344">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="029aa-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="029aa-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="029aa-346">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="029aa-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="029aa-347">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="029aa-347">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-348">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="029aa-348">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="029aa-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="029aa-350">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="029aa-350">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="029aa-351">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="029aa-351">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="029aa-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="029aa-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="029aa-353"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="029aa-353"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="029aa-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="029aa-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="029aa-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="029aa-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-356">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="029aa-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="029aa-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="029aa-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-358">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="029aa-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="029aa-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="029aa-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-360">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="029aa-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="029aa-361">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="029aa-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="029aa-362">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="029aa-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="029aa-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="029aa-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-364">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="029aa-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="029aa-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="029aa-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="029aa-366">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="029aa-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="029aa-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="029aa-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-368">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="029aa-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="029aa-370">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="029aa-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="029aa-371">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="029aa-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="029aa-372">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="029aa-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="029aa-373">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="029aa-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="029aa-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-375">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="029aa-375">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="029aa-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-378">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Port de bus DMTF \| 001,2 "," MIF. \|Disques DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="029aa-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-379">Protocole utilisé par le contrôleur pour accéder aux appareils « contrôlés ».</span><span class="sxs-lookup"><span data-stu-id="029aa-379">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="029aa-380">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-380">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="029aa-381">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="029aa-381">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="029aa-382">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="029aa-382">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="029aa-383">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="029aa-383">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="029aa-384">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="029aa-384">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="029aa-385">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="029aa-385">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="029aa-386">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="029aa-386">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="029aa-387">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="029aa-387">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="029aa-388">**Disquette flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="029aa-388">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="029aa-389">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="029aa-389">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="029aa-390">**Interface parallèle SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="029aa-390">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="029aa-391">**Protocole SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="029aa-391">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="029aa-392">**Protocole de bus série SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="029aa-392">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="029aa-393">**Protocole serial bus SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="029aa-393">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="029aa-394">**Architecture de stockage en série SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="029aa-394">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="029aa-395">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="029aa-395">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="029aa-396">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="029aa-396">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="029aa-397">**Bus série universel** (16)</span><span class="sxs-lookup"><span data-stu-id="029aa-397">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="029aa-398">**Protocole parallèle** (17)</span><span class="sxs-lookup"><span data-stu-id="029aa-398">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="029aa-399">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="029aa-399">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="029aa-400">**Diagnostic** (19)</span><span class="sxs-lookup"><span data-stu-id="029aa-400">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="029aa-401">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="029aa-401">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="029aa-402">**Puissance** (21)</span><span class="sxs-lookup"><span data-stu-id="029aa-402">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="029aa-403">**HIPPA** (22)</span><span class="sxs-lookup"><span data-stu-id="029aa-403">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="029aa-404">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="029aa-404">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="029aa-405">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="029aa-405">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="029aa-406">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="029aa-406">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="029aa-407">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="029aa-407">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="029aa-408">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="029aa-408">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="029aa-409">**IEEE 802,3 10Base5** (28)</span><span class="sxs-lookup"><span data-stu-id="029aa-409">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="029aa-410">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="029aa-410">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="029aa-411">**IEEE 802,3 1Base5** (30)</span><span class="sxs-lookup"><span data-stu-id="029aa-411">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="029aa-412">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="029aa-412">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="029aa-413">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="029aa-413">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="029aa-414">**Token Ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="029aa-414">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="029aa-415">**ANSI x3t 9.5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="029aa-415">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="029aa-416">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="029aa-416">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="029aa-417">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="029aa-417">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="029aa-418">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="029aa-418">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="029aa-419">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="029aa-419">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="029aa-420">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="029aa-420">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="029aa-421">**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="029aa-421">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="029aa-422">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="029aa-422">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="029aa-423">**ATA/IDE amélioré** (42)</span><span class="sxs-lookup"><span data-stu-id="029aa-423">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="029aa-424">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="029aa-424">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="029aa-425">**TWIRP (infrarouge bidirectionnel)** (44)</span><span class="sxs-lookup"><span data-stu-id="029aa-425">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="029aa-426">**FIR (infrarouge rapide)** (45)</span><span class="sxs-lookup"><span data-stu-id="029aa-426">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="029aa-427">**Sir (infrarouge série)** (46)</span><span class="sxs-lookup"><span data-stu-id="029aa-427">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="029aa-428">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="029aa-428">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="029aa-429">**État**</span><span class="sxs-lookup"><span data-stu-id="029aa-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-432">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="029aa-432">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-433">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="029aa-433">Current status of the object.</span></span> <span data-ttu-id="029aa-434">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-434">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="029aa-435">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="029aa-435">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="029aa-436">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="029aa-436">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="029aa-437">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="029aa-437">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="029aa-438">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="029aa-438">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="029aa-439">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="029aa-439">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="029aa-440">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="029aa-440">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="029aa-441">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="029aa-441">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="029aa-442">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="029aa-442">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="029aa-443">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="029aa-443">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="029aa-444">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="029aa-444">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="029aa-445">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="029aa-445">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="029aa-446">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="029aa-446">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="029aa-447">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="029aa-447">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="029aa-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="029aa-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-449">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="029aa-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-451">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="029aa-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="029aa-452">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="029aa-452">State of the logical device.</span></span> <span data-ttu-id="029aa-453">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="029aa-453">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="029aa-454">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="029aa-455">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="029aa-455">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="029aa-456">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="029aa-456">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="029aa-457">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="029aa-457">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="029aa-458">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="029aa-458">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="029aa-459">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="029aa-459">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="029aa-460">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="029aa-460">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-461">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-462">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-463">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="029aa-463">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="029aa-464">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="029aa-464">Scoping system's creation class name.</span></span>

<span data-ttu-id="029aa-465">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-466">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="029aa-466">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-467">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="029aa-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-468">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="029aa-469">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="029aa-469">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="029aa-470">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="029aa-470">Scoping system's name.</span></span>

<span data-ttu-id="029aa-471">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-471">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="029aa-472">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="029aa-472">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="029aa-473">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="029aa-473">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="029aa-474">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="029aa-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="029aa-475">Date et heure de la dernière réinitialisation du contrôleur, ce qui signifie que le contrôleur a été mis hors tension ou réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="029aa-475">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="029aa-476">Cette propriété est héritée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-476">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="029aa-477">Notes</span><span class="sxs-lookup"><span data-stu-id="029aa-477">Remarks</span></span>

<span data-ttu-id="029aa-478">La classe **CIM \_ USBController** est dérivée [**du \_ contrôleur CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-478">The **CIM\_USBController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="029aa-479">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="029aa-479">WMI does not implement this class.</span></span> <span data-ttu-id="029aa-480">Pour les classes WMI dérivées de **CIM \_ USBController**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="029aa-480">For WMI classes derived from **CIM\_USBController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="029aa-481">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="029aa-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="029aa-482">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="029aa-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="029aa-483">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="029aa-483">Requirements</span></span>



| <span data-ttu-id="029aa-484">Condition requise</span><span class="sxs-lookup"><span data-stu-id="029aa-484">Requirement</span></span> | <span data-ttu-id="029aa-485">Valeur</span><span class="sxs-lookup"><span data-stu-id="029aa-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="029aa-486">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="029aa-486">Minimum supported client</span></span><br/> | <span data-ttu-id="029aa-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="029aa-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="029aa-488">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="029aa-488">Minimum supported server</span></span><br/> | <span data-ttu-id="029aa-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="029aa-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="029aa-490">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="029aa-490">Namespace</span></span><br/>                | <span data-ttu-id="029aa-491">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="029aa-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="029aa-492">MOF</span><span class="sxs-lookup"><span data-stu-id="029aa-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="029aa-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="029aa-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="029aa-494">DLL</span><span class="sxs-lookup"><span data-stu-id="029aa-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="029aa-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="029aa-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029aa-496">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="029aa-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029aa-497">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="029aa-497">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

