---
description: La \_ classe de ventilateur CIM représente les fonctionnalités et la gestion d’un appareil de refroidissement de ventilateur.
ms.assetid: eddfb694-cba1-45e2-998f-f93355520c80
ms.tgt_platform: multiple
title: Classe CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan
- CIM_Fan.ActiveCooling
- CIM_Fan.Availability
- CIM_Fan.Caption
- CIM_Fan.ConfigManagerErrorCode
- CIM_Fan.ConfigManagerUserConfig
- CIM_Fan.CreationClassName
- CIM_Fan.Description
- CIM_Fan.DesiredSpeed
- CIM_Fan.DeviceID
- CIM_Fan.ErrorCleared
- CIM_Fan.ErrorDescription
- CIM_Fan.InstallDate
- CIM_Fan.LastErrorCode
- CIM_Fan.Name
- CIM_Fan.PNPDeviceID
- CIM_Fan.PowerManagementCapabilities
- CIM_Fan.PowerManagementSupported
- CIM_Fan.Status
- CIM_Fan.StatusInfo
- CIM_Fan.SystemCreationClassName
- CIM_Fan.SystemName
- CIM_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a06e0ddebbdadf7cb4e6dd61afa3fa7c178f661
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861261"
---
# <a name="cim_fan-class"></a><span data-ttu-id="2d560-103">\_Classe de ventilateur CIM</span><span class="sxs-lookup"><span data-stu-id="2d560-103">CIM\_Fan class</span></span>

<span data-ttu-id="2d560-104">La classe de **\_ ventilateur CIM** représente les fonctionnalités et la gestion d’un appareil de refroidissement de ventilateur.</span><span class="sxs-lookup"><span data-stu-id="2d560-104">The **CIM\_Fan** class represents the capabilities and management of a fan cooling device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d560-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="2d560-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2d560-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2d560-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2d560-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2d560-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2d560-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="2d560-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d560-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d560-109">Syntax</span></span>

``` syntax
[UUID("{0A59C856-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Fan : CIM_CoolingDevice
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="2d560-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2d560-110">Members</span></span>

<span data-ttu-id="2d560-111">La classe de **\_ ventilateur CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2d560-111">The **CIM\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="2d560-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d560-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d560-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d560-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d560-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2d560-114">Methods</span></span>

<span data-ttu-id="2d560-115">La classe de **\_ ventilateur CIM** présente ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2d560-115">The **CIM\_Fan** class has these methods.</span></span>



| <span data-ttu-id="2d560-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2d560-116">Method</span></span>                                                         | <span data-ttu-id="2d560-117">Description</span><span class="sxs-lookup"><span data-stu-id="2d560-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d560-118">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="2d560-118">**Reset**</span></span>](reset-method-in-class-cim-fan.md)                 | <span data-ttu-id="2d560-119">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d560-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="2d560-120">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2d560-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="2d560-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2d560-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-fan.md) | <span data-ttu-id="2d560-122">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="2d560-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="2d560-123">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2d560-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="2d560-124">**SetSpeed**</span><span class="sxs-lookup"><span data-stu-id="2d560-124">**SetSpeed**</span></span>](setspeed-method-in-class-cim-fan.md)           | <span data-ttu-id="2d560-125">Définit la vitesse du ventilateur.</span><span class="sxs-lookup"><span data-stu-id="2d560-125">Sets the fan speed.</span></span> <span data-ttu-id="2d560-126">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="2d560-126">Not implemented by WMI.</span></span><br/>                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="2d560-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2d560-127">Properties</span></span>

<span data-ttu-id="2d560-128">La classe de **\_ ventilateur CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2d560-128">The **CIM\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d560-129">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="2d560-129">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-130">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d560-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-132">Si la **valeur est true**, l’appareil de refroidissement fournit le refroidissement actif (par opposition à passif).</span><span class="sxs-lookup"><span data-stu-id="2d560-132">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="2d560-133">Cette propriété est héritée de la [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-133">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-134">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="2d560-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d560-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-137">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2d560-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-138">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-138">Availability and status of the device.</span></span>

<span data-ttu-id="2d560-139">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2d560-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2d560-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d560-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2d560-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2d560-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="2d560-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2d560-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="2d560-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2d560-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="2d560-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2d560-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2d560-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2d560-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="2d560-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2d560-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="2d560-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2d560-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="2d560-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2d560-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="2d560-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2d560-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="2d560-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2d560-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="2d560-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2d560-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="2d560-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-153">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2d560-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2d560-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="2d560-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-155">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="2d560-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2d560-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="2d560-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-157">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="2d560-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2d560-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="2d560-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2d560-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="2d560-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-160">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="2d560-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2d560-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="2d560-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-162">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="2d560-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2d560-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="2d560-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-164">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="2d560-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2d560-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="2d560-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-166">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="2d560-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2d560-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="2d560-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-168">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="2d560-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d560-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2d560-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-172">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2d560-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-173">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d560-173">Short textual description of the object.</span></span>

<span data-ttu-id="2d560-174">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2d560-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-176">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d560-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-178">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2d560-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-179">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2d560-179">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="2d560-180">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2d560-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="2d560-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2d560-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="2d560-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-183">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="2d560-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2d560-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="2d560-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2d560-185">(1)</span><span class="sxs-lookup"><span data-stu-id="2d560-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-186">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="2d560-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2d560-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2d560-188">(2)</span><span class="sxs-lookup"><span data-stu-id="2d560-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2d560-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="2d560-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2d560-190">(3)</span><span class="sxs-lookup"><span data-stu-id="2d560-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-191">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="2d560-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2d560-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="2d560-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2d560-193">(4)</span><span class="sxs-lookup"><span data-stu-id="2d560-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-194">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="2d560-194">Device is not working properly.</span></span> <span data-ttu-id="2d560-195">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="2d560-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2d560-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="2d560-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2d560-197">(5)</span><span class="sxs-lookup"><span data-stu-id="2d560-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-198">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="2d560-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2d560-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="2d560-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2d560-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="2d560-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-201">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="2d560-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2d560-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="2d560-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2d560-203">(7)</span><span class="sxs-lookup"><span data-stu-id="2d560-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2d560-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="2d560-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2d560-205">(8)</span><span class="sxs-lookup"><span data-stu-id="2d560-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-206">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="2d560-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2d560-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2d560-208">(9)</span><span class="sxs-lookup"><span data-stu-id="2d560-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-209">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2d560-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2d560-211">(10)</span><span class="sxs-lookup"><span data-stu-id="2d560-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-212">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2d560-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2d560-214">(11)</span><span class="sxs-lookup"><span data-stu-id="2d560-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-215">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2d560-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="2d560-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2d560-217">douze</span><span class="sxs-lookup"><span data-stu-id="2d560-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-218">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2d560-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2d560-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2d560-220">(13)</span><span class="sxs-lookup"><span data-stu-id="2d560-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-221">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2d560-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="2d560-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2d560-223">(14)</span><span class="sxs-lookup"><span data-stu-id="2d560-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-224">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="2d560-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2d560-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="2d560-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2d560-226">(15)</span><span class="sxs-lookup"><span data-stu-id="2d560-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-227">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="2d560-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2d560-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2d560-229">(16)</span><span class="sxs-lookup"><span data-stu-id="2d560-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-230">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2d560-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="2d560-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2d560-232">(17)</span><span class="sxs-lookup"><span data-stu-id="2d560-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-233">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="2d560-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2d560-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2d560-235">(18)</span><span class="sxs-lookup"><span data-stu-id="2d560-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-236">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="2d560-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2d560-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="2d560-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2d560-238">(19)</span><span class="sxs-lookup"><span data-stu-id="2d560-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2d560-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="2d560-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2d560-240">(20)</span><span class="sxs-lookup"><span data-stu-id="2d560-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-241">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="2d560-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2d560-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2d560-243">(21)</span><span class="sxs-lookup"><span data-stu-id="2d560-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-244">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="2d560-244">System failure.</span></span> <span data-ttu-id="2d560-245">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="2d560-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2d560-246">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2d560-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="2d560-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2d560-248">(22)</span><span class="sxs-lookup"><span data-stu-id="2d560-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-249">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2d560-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2d560-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="2d560-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2d560-251">(23)</span><span class="sxs-lookup"><span data-stu-id="2d560-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-252">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="2d560-252">System failure.</span></span> <span data-ttu-id="2d560-253">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="2d560-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2d560-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="2d560-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2d560-255">(24)</span><span class="sxs-lookup"><span data-stu-id="2d560-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-256">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="2d560-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2d560-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2d560-258">(25)</span><span class="sxs-lookup"><span data-stu-id="2d560-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-259">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2d560-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2d560-261">(26)</span><span class="sxs-lookup"><span data-stu-id="2d560-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-262">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2d560-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="2d560-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2d560-264">(27)</span><span class="sxs-lookup"><span data-stu-id="2d560-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-265">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="2d560-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2d560-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="2d560-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2d560-267">(28)</span><span class="sxs-lookup"><span data-stu-id="2d560-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-268">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="2d560-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2d560-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="2d560-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2d560-270">(29)</span><span class="sxs-lookup"><span data-stu-id="2d560-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-271">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="2d560-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2d560-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="2d560-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2d560-273">(30)</span><span class="sxs-lookup"><span data-stu-id="2d560-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-274">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="2d560-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2d560-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="2d560-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2d560-276">31</span><span class="sxs-lookup"><span data-stu-id="2d560-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-277">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="2d560-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d560-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2d560-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-279">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d560-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-281">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2d560-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-282">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d560-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2d560-283">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d560-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-287">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2d560-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2d560-288">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="2d560-288">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2d560-289">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="2d560-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2d560-290">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-291">**Description**</span><span class="sxs-lookup"><span data-stu-id="2d560-291">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-294">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2d560-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-295">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d560-295">Textual description of the object.</span></span>

<span data-ttu-id="2d560-296">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-296">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-297">**DesiredSpeed**</span><span class="sxs-lookup"><span data-stu-id="2d560-297">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-298">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2d560-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-300">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« tours par minute »)</span><span class="sxs-lookup"><span data-stu-id="2d560-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-301">Vitesse de ventilateur demandée, définie en tours par minute, lorsqu’un ventilateur à vitesse variable est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2d560-301">Requested fan speed, defined in revolutions per minute, when a variable speed fan is supported.</span></span> <span data-ttu-id="2d560-302">La vitesse actuelle est déterminée par un capteur ([**le \_ tachymètre CIM**](cim-tachometer.md)) associé au ventilateur à l’aide de la relation [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="2d560-302">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="2d560-303">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2d560-303">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-304">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2d560-304">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-307">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2d560-307">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2d560-308">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d560-308">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2d560-309">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2d560-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-311">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d560-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-313">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="2d560-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2d560-314">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2d560-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-318">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="2d560-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2d560-319">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-320">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2d560-320">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-321">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2d560-321">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-323">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2d560-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-324">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d560-324">Date and time the object was installed.</span></span> <span data-ttu-id="2d560-325">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="2d560-325">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2d560-326">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-327">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2d560-327">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-328">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d560-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-330">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d560-330">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2d560-331">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-332">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2d560-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-335">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2d560-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-336">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2d560-336">Label by which the object is known.</span></span> <span data-ttu-id="2d560-337">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="2d560-337">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2d560-338">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2d560-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-342">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2d560-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-343">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d560-343">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="2d560-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2d560-345">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="2d560-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2d560-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2d560-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-347">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d560-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2d560-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-349">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="2d560-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2d560-350">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="2d560-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d560-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2d560-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2d560-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="2d560-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-353">Les capacités liées à l’alimentation ne sont pas prises en charge pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2d560-353">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2d560-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="2d560-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2d560-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="2d560-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-356">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="2d560-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2d560-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="2d560-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-358">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="2d560-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2d560-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="2d560-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-360">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2d560-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2d560-361">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="2d560-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2d560-362">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2d560-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2d560-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="2d560-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-364">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="2d560-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2d560-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="2d560-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2d560-366">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="2d560-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d560-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2d560-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-368">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d560-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-370">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="2d560-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2d560-371">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2d560-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2d560-372">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2d560-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2d560-373">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2d560-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="2d560-374">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-375">**État**</span><span class="sxs-lookup"><span data-stu-id="2d560-375">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-378">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2d560-378">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-379">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2d560-379">Current status of the object.</span></span> <span data-ttu-id="2d560-380">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2d560-381">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d560-381">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2d560-382">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2d560-382">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2d560-383">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2d560-383">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2d560-384">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2d560-384">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d560-385">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2d560-385">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2d560-386">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2d560-386">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2d560-387">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2d560-387">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2d560-388">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2d560-388">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2d560-389">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2d560-389">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2d560-390">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2d560-390">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2d560-391">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2d560-391">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2d560-392">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2d560-392">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2d560-393">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2d560-393">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d560-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2d560-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-395">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2d560-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-397">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2d560-397">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2d560-398">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2d560-398">State of the logical device.</span></span> <span data-ttu-id="2d560-399">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="2d560-399">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2d560-400">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2d560-401">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="2d560-401">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2d560-402">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="2d560-402">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2d560-403">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="2d560-403">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2d560-404">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="2d560-404">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2d560-405">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2d560-405">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d560-406">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2d560-406">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-407">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-409">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2d560-409">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2d560-410">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2d560-410">Scoping system's creation class name.</span></span>

<span data-ttu-id="2d560-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-412">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2d560-412">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-413">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2d560-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d560-415">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2d560-415">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2d560-416">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2d560-416">Scoping system's name.</span></span>

<span data-ttu-id="2d560-417">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d560-418">**VariableSpeed**</span><span class="sxs-lookup"><span data-stu-id="2d560-418">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d560-419">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2d560-419">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d560-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2d560-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d560-421">Si la **valeur est true**, le ventilateur prend en charge des vitesses variables.</span><span class="sxs-lookup"><span data-stu-id="2d560-421">If **TRUE**, the fan supports variable speeds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d560-422">Notes</span><span class="sxs-lookup"><span data-stu-id="2d560-422">Remarks</span></span>

<span data-ttu-id="2d560-423">La classe de **\_ ventilateur CIM** est dérivée de la [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-423">The **CIM\_Fan** class is derived from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

<span data-ttu-id="2d560-424">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="2d560-424">WMI does not implement this class.</span></span> <span data-ttu-id="2d560-425">Pour les classes dérivées du **\_ ventilateur CIM**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2d560-425">For classes derived from **CIM\_Fan**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="2d560-426">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="2d560-426">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2d560-427">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="2d560-427">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d560-428">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d560-428">Requirements</span></span>



| <span data-ttu-id="2d560-429">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d560-429">Requirement</span></span> | <span data-ttu-id="2d560-430">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d560-430">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d560-431">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d560-431">Minimum supported client</span></span><br/> | <span data-ttu-id="2d560-432">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d560-432">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d560-433">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d560-433">Minimum supported server</span></span><br/> | <span data-ttu-id="2d560-434">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d560-434">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d560-435">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d560-435">Namespace</span></span><br/>                | <span data-ttu-id="2d560-436">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2d560-436">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d560-437">MOF</span><span class="sxs-lookup"><span data-stu-id="2d560-437">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d560-438"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d560-438"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d560-439">DLL</span><span class="sxs-lookup"><span data-stu-id="2d560-439">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d560-440"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d560-440"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d560-441">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d560-441">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d560-442">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2d560-442">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> </dl>

 

