---
description: La \_ classe CIM CoolingDevice représente les fonctionnalités et la gestion des appareils de refroidissement.
ms.assetid: ac0f0df4-c174-4306-9325-eaa316ee820a
ms.tgt_platform: multiple
title: Classe CIM_CoolingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CoolingDevice
- CIM_CoolingDevice.Caption
- CIM_CoolingDevice.Description
- CIM_CoolingDevice.InstallDate
- CIM_CoolingDevice.Name
- CIM_CoolingDevice.Status
- CIM_CoolingDevice.Availability
- CIM_CoolingDevice.ConfigManagerErrorCode
- CIM_CoolingDevice.ConfigManagerUserConfig
- CIM_CoolingDevice.CreationClassName
- CIM_CoolingDevice.DeviceID
- CIM_CoolingDevice.PowerManagementCapabilities
- CIM_CoolingDevice.ErrorCleared
- CIM_CoolingDevice.ErrorDescription
- CIM_CoolingDevice.LastErrorCode
- CIM_CoolingDevice.PNPDeviceID
- CIM_CoolingDevice.PowerManagementSupported
- CIM_CoolingDevice.StatusInfo
- CIM_CoolingDevice.SystemCreationClassName
- CIM_CoolingDevice.SystemName
- CIM_CoolingDevice.ActiveCooling
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f6c480e910cf72a319856942fda28d2139d0a6ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514110"
---
# <a name="cim_coolingdevice-class"></a><span data-ttu-id="a2297-103">\_Classe CIM CoolingDevice</span><span class="sxs-lookup"><span data-stu-id="a2297-103">CIM\_CoolingDevice class</span></span>

<span data-ttu-id="a2297-104">La classe **CIM \_ CoolingDevice** représente les fonctionnalités et la gestion des appareils de refroidissement.</span><span class="sxs-lookup"><span data-stu-id="a2297-104">The **CIM\_CoolingDevice** class represents the capabilities and management of cooling devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2297-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="a2297-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a2297-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a2297-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a2297-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a2297-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a2297-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="a2297-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2297-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2297-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979A-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_CoolingDevice : CIM_LogicalDevice
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
  boolean  ActiveCooling;
};
```

## <a name="members"></a><span data-ttu-id="a2297-110">Membres</span><span class="sxs-lookup"><span data-stu-id="a2297-110">Members</span></span>

<span data-ttu-id="a2297-111">La classe **CIM \_ CoolingDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a2297-111">The **CIM\_CoolingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="a2297-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a2297-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a2297-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2297-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a2297-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a2297-114">Methods</span></span>

<span data-ttu-id="a2297-115">La classe **CIM \_ CoolingDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a2297-115">The **CIM\_CoolingDevice** class has these methods.</span></span>



| <span data-ttu-id="a2297-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="a2297-116">Method</span></span>                                                                   | <span data-ttu-id="a2297-117">Description</span><span class="sxs-lookup"><span data-stu-id="a2297-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2297-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="a2297-118">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                    | <span data-ttu-id="a2297-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a2297-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="a2297-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a2297-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a2297-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a2297-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-coolingdevice.md) | <span data-ttu-id="a2297-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="a2297-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a2297-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="a2297-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a2297-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a2297-124">Properties</span></span>

<span data-ttu-id="a2297-125">La classe **CIM \_ CoolingDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2297-125">The **CIM\_CoolingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2297-126">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="a2297-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a2297-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2297-129">Si la **valeur est true**, l’appareil de refroidissement fournit le refroidissement actif (par opposition à passif).</span><span class="sxs-lookup"><span data-stu-id="a2297-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

</dd> <dt>

<span data-ttu-id="a2297-130">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="a2297-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-131">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2297-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-133">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a2297-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-134">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a2297-134">Availability and status of the device.</span></span>

<span data-ttu-id="a2297-135">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2297-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a2297-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2297-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a2297-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a2297-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="a2297-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a2297-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="a2297-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a2297-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="a2297-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a2297-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a2297-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a2297-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="a2297-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a2297-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="a2297-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a2297-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="a2297-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a2297-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="a2297-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a2297-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="a2297-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a2297-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="a2297-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a2297-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="a2297-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-149">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="a2297-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a2297-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="a2297-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-151">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="a2297-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a2297-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="a2297-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-153">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="a2297-153">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a2297-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="a2297-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a2297-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="a2297-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-156">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="a2297-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a2297-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="a2297-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-158">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="a2297-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a2297-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="a2297-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-160">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="a2297-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a2297-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="a2297-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-162">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="a2297-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a2297-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="a2297-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-164">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="a2297-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a2297-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a2297-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-168">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="a2297-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-169">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a2297-169">A short textual description of the object.</span></span>

<span data-ttu-id="a2297-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a2297-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2297-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-174">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a2297-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-175">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="a2297-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a2297-176">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a2297-177">**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="a2297-177">**This device is working properly.**</span></span> <span data-ttu-id="a2297-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="a2297-178">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a2297-179">**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="a2297-179">**This device is not configured correctly.**</span></span> <span data-ttu-id="a2297-180">(1)</span><span class="sxs-lookup"><span data-stu-id="a2297-180">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a2297-181">**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-181">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a2297-182">(2)</span><span class="sxs-lookup"><span data-stu-id="a2297-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a2297-183">**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="a2297-183">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a2297-184">(3)</span><span class="sxs-lookup"><span data-stu-id="a2297-184">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a2297-185">**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="a2297-185">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a2297-186">(4)</span><span class="sxs-lookup"><span data-stu-id="a2297-186">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a2297-187">**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="a2297-187">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a2297-188">(5)</span><span class="sxs-lookup"><span data-stu-id="a2297-188">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a2297-189">**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="a2297-189">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a2297-190"> (6)</span><span class="sxs-lookup"><span data-stu-id="a2297-190">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a2297-191">**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="a2297-191">**Cannot filter.**</span></span> <span data-ttu-id="a2297-192">(7)</span><span class="sxs-lookup"><span data-stu-id="a2297-192">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a2297-193">**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="a2297-193">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a2297-194">(8)</span><span class="sxs-lookup"><span data-stu-id="a2297-194">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a2297-195">**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-195">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a2297-196">(9)</span><span class="sxs-lookup"><span data-stu-id="a2297-196">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a2297-197">**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-197">**This device cannot start.**</span></span> <span data-ttu-id="a2297-198">(10)</span><span class="sxs-lookup"><span data-stu-id="a2297-198">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a2297-199">**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-199">**This device failed.**</span></span> <span data-ttu-id="a2297-200">(11)</span><span class="sxs-lookup"><span data-stu-id="a2297-200">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a2297-201">**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="a2297-201">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a2297-202">douze</span><span class="sxs-lookup"><span data-stu-id="a2297-202">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a2297-203">**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-203">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a2297-204">(13)</span><span class="sxs-lookup"><span data-stu-id="a2297-204">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a2297-205">**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="a2297-205">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a2297-206">(14)</span><span class="sxs-lookup"><span data-stu-id="a2297-206">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a2297-207">**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="a2297-207">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a2297-208">(15)</span><span class="sxs-lookup"><span data-stu-id="a2297-208">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a2297-209">**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-209">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a2297-210">(16)</span><span class="sxs-lookup"><span data-stu-id="a2297-210">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a2297-211">**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="a2297-211">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a2297-212">(17)</span><span class="sxs-lookup"><span data-stu-id="a2297-212">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a2297-213">**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-213">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a2297-214">(18)</span><span class="sxs-lookup"><span data-stu-id="a2297-214">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a2297-215">**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="a2297-215">**Failure using the VxD loader.**</span></span> <span data-ttu-id="a2297-216">(19)</span><span class="sxs-lookup"><span data-stu-id="a2297-216">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a2297-217">**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="a2297-217">**Your registry might be corrupted.**</span></span> <span data-ttu-id="a2297-218">(20)</span><span class="sxs-lookup"><span data-stu-id="a2297-218">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a2297-219">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-219">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a2297-220">(21)</span><span class="sxs-lookup"><span data-stu-id="a2297-220">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a2297-221">**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="a2297-221">**This device is disabled.**</span></span> <span data-ttu-id="a2297-222">(22)</span><span class="sxs-lookup"><span data-stu-id="a2297-222">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a2297-223">**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="a2297-223">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a2297-224">(23)</span><span class="sxs-lookup"><span data-stu-id="a2297-224">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a2297-225">**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="a2297-225">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a2297-226">(24)</span><span class="sxs-lookup"><span data-stu-id="a2297-226">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a2297-227">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a2297-228">(25)</span><span class="sxs-lookup"><span data-stu-id="a2297-228">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a2297-229">**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a2297-230">(26)</span><span class="sxs-lookup"><span data-stu-id="a2297-230">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a2297-231">**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="a2297-231">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a2297-232">(27)</span><span class="sxs-lookup"><span data-stu-id="a2297-232">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a2297-233">**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="a2297-233">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a2297-234">(28)</span><span class="sxs-lookup"><span data-stu-id="a2297-234">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a2297-235">**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="a2297-235">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a2297-236">(29)</span><span class="sxs-lookup"><span data-stu-id="a2297-236">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a2297-237">**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="a2297-237">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a2297-238">(30)</span><span class="sxs-lookup"><span data-stu-id="a2297-238">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a2297-239">**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="a2297-239">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a2297-240">31</span><span class="sxs-lookup"><span data-stu-id="a2297-240">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2297-241">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a2297-241">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-242">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a2297-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-244">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a2297-244">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-245">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2297-245">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a2297-246">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-246">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-247">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2297-247">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-250">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2297-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2297-251">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="a2297-251">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a2297-252">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="a2297-252">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a2297-253">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-253">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-254">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2297-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-257">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a2297-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-258">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a2297-258">A textual description of the object.</span></span>

<span data-ttu-id="a2297-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-260">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a2297-260">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-263">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2297-263">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2297-264">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a2297-264">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a2297-265">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-266">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a2297-266">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-267">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a2297-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2297-269">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="a2297-269">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a2297-270">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-271">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a2297-271">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2297-274">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="a2297-274">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a2297-275">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a2297-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-277">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2297-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-279">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="a2297-279">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-280">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="a2297-280">Indicates when the object was installed.</span></span> <span data-ttu-id="a2297-281">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="a2297-281">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a2297-282">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-283">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a2297-283">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-284">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2297-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2297-286">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a2297-286">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a2297-287">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-288">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a2297-288">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-291">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a2297-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-292">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="a2297-292">Label by which the object is known.</span></span> <span data-ttu-id="a2297-293">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="a2297-293">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a2297-294">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-295">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a2297-295">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-298">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a2297-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-299">Indique l’identificateur d’appareil Plug-and-Play Win32 de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="a2297-299">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a2297-300">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="a2297-300">Example: "\*PNP030b"</span></span>

<span data-ttu-id="a2297-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-302">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a2297-302">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-303">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2297-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2297-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2297-305">Indique les fonctionnalités de gestion de l’alimentation spécifiques de l’appareil logique.</span><span class="sxs-lookup"><span data-stu-id="a2297-305">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="a2297-306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2297-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="a2297-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-308">Les capacités associées à l’alimentation sont inconnues.</span><span class="sxs-lookup"><span data-stu-id="a2297-308">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a2297-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="a2297-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-310">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="a2297-310">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a2297-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="a2297-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-312">Les capacités associées à l’alimentation ont été désactivées.</span><span class="sxs-lookup"><span data-stu-id="a2297-312">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a2297-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="a2297-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-314">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="a2297-314">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a2297-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="a2297-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-316">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="a2297-316">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a2297-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="a2297-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-318">La méthode **SetPowerState** est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a2297-318">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="a2297-319">Cette méthode se trouve sur la classe parente du [**\_ LogicalDevice CIM**](cim-logicaldevice.md) et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="a2297-319">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="a2297-320">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a2297-320">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a2297-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="a2297-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-322">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle »).</span><span class="sxs-lookup"><span data-stu-id="a2297-322">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a2297-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="a2297-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a2297-324">La méthode **SetPowerState** peut être appelée avec le paramètre *PowerState* défini sur 5 (« Power cycle ») et le paramètre *Time* défini sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="a2297-324">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a2297-325">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a2297-325">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-326">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a2297-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2297-328">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="a2297-328">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a2297-329">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a2297-329">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a2297-330">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a2297-330">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a2297-331">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a2297-331">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a2297-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-333">**État**</span><span class="sxs-lookup"><span data-stu-id="a2297-333">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-336">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a2297-336">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-337">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a2297-337">String that indicates the current status of the object.</span></span> <span data-ttu-id="a2297-338">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="a2297-338">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a2297-339">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="a2297-339">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a2297-340">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="a2297-340">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a2297-341">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="a2297-341">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a2297-342">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="a2297-342">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a2297-343">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="a2297-343">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a2297-344">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a2297-345">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2297-345">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a2297-346">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="a2297-346">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a2297-347">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="a2297-347">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a2297-348">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="a2297-348">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2297-349">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="a2297-349">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a2297-350">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="a2297-350">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a2297-351">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="a2297-351">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a2297-352">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="a2297-352">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a2297-353">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="a2297-353">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a2297-354">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="a2297-354">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a2297-355">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="a2297-355">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a2297-356">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="a2297-356">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a2297-357">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="a2297-357">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2297-358">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a2297-358">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-359">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2297-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-361">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a2297-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a2297-362">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a2297-362">State of the logical device.</span></span> <span data-ttu-id="a2297-363">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (« non applicable ») doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="a2297-363">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="a2297-364">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2297-365">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="a2297-365">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2297-366">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="a2297-366">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a2297-367">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="a2297-367">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a2297-368">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="a2297-368">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a2297-369">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="a2297-369">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2297-370">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2297-370">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-371">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-373">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2297-373">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2297-374">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a2297-374">The scoping system's creation class name.</span></span>

<span data-ttu-id="a2297-375">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2297-376">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a2297-376">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2297-377">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a2297-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2297-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a2297-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2297-379">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2297-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2297-380">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="a2297-380">The scoping system's name.</span></span>

<span data-ttu-id="a2297-381">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2297-382">Notes</span><span class="sxs-lookup"><span data-stu-id="a2297-382">Remarks</span></span>

<span data-ttu-id="a2297-383">La classe **CIM \_ CoolingDevice** est dérivée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-383">The **CIM\_CoolingDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a2297-384">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="a2297-384">WMI does not implement this class.</span></span> <span data-ttu-id="a2297-385">Pour les classes dérivées de **CIM \_ CoolingDevice**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a2297-385">For classes derived from **CIM\_CoolingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a2297-386">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="a2297-386">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a2297-387">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a2297-387">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2297-388">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2297-388">Requirements</span></span>



| <span data-ttu-id="a2297-389">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2297-389">Requirement</span></span> | <span data-ttu-id="a2297-390">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2297-390">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2297-391">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2297-391">Minimum supported client</span></span><br/> | <span data-ttu-id="a2297-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2297-392">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2297-393">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2297-393">Minimum supported server</span></span><br/> | <span data-ttu-id="a2297-394">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2297-394">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2297-395">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a2297-395">Namespace</span></span><br/>                | <span data-ttu-id="a2297-396">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a2297-396">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2297-397">MOF</span><span class="sxs-lookup"><span data-stu-id="a2297-397">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2297-398"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2297-398"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2297-399">DLL</span><span class="sxs-lookup"><span data-stu-id="a2297-399">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2297-400"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2297-400"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2297-401">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2297-401">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2297-402">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="a2297-402">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

