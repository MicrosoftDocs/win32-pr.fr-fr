---
description: La classe de la \_ carte CIM est une classe abstraite qui définit les concepts généraux de matériel de mise en réseau (par exemple, une adresse permanente ou une vitesse de fonctionnement). Les informations sont transmises à l’aide de l' \_ Association CIM DeviceSAPImplementation.
ms.assetid: dd44e05a-1124-42c2-aa69-340c06da35a2
ms.tgt_platform: multiple
title: Classe CIM_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter
- CIM_NetworkAdapter.AutoSense
- CIM_NetworkAdapter.Availability
- CIM_NetworkAdapter.Caption
- CIM_NetworkAdapter.ConfigManagerErrorCode
- CIM_NetworkAdapter.ConfigManagerUserConfig
- CIM_NetworkAdapter.CreationClassName
- CIM_NetworkAdapter.Description
- CIM_NetworkAdapter.DeviceID
- CIM_NetworkAdapter.ErrorCleared
- CIM_NetworkAdapter.ErrorDescription
- CIM_NetworkAdapter.InstallDate
- CIM_NetworkAdapter.LastErrorCode
- CIM_NetworkAdapter.MaxSpeed
- CIM_NetworkAdapter.Name
- CIM_NetworkAdapter.NetworkAddresses
- CIM_NetworkAdapter.PermanentAddress
- CIM_NetworkAdapter.PNPDeviceID
- CIM_NetworkAdapter.PowerManagementCapabilities
- CIM_NetworkAdapter.PowerManagementSupported
- CIM_NetworkAdapter.Speed
- CIM_NetworkAdapter.Status
- CIM_NetworkAdapter.StatusInfo
- CIM_NetworkAdapter.SystemCreationClassName
- CIM_NetworkAdapter.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76ec70bb74d74514dfe037c9e67604b29aee541a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110958"
---
# <a name="cim_networkadapter-class"></a><span data-ttu-id="6df7c-104">\_Classe NETWORKADAPTER CIM</span><span class="sxs-lookup"><span data-stu-id="6df7c-104">CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="6df7c-105">La classe de la carte CIM est une classe abstraite qui définit les concepts généraux de matériel de mise en réseau (par exemple, une adresse permanente ou une vitesse de fonctionnement). **\_**</span><span class="sxs-lookup"><span data-stu-id="6df7c-105">The **CIM\_NetworkAdapter** class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="6df7c-106">Les informations sont transmises à l’aide de l’Association [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="6df7c-106">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

<span data-ttu-id="6df7c-107">Les cartes réseau et les points de terminaison associés représentent le potentiel pour la connectivité entre pairs.</span><span class="sxs-lookup"><span data-stu-id="6df7c-107">Network adapters and related endpoints represent the potential for connectivity among peers.</span></span> <span data-ttu-id="6df7c-108">Le potentiel de connectivité est très différent de celui des relations maître ou subordonné, ou contrôlé par le contrôleur [**CIM \_**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-108">The potential for connectivity is significantly different from the master or subordinate and controller or controlled-by relationships of [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="6df7c-109">Toutefois, il peut arriver qu’un seul appareil fasse office de carte réseau et de contrôleur, par exemple lorsqu’une carte Fibre Channel fonctionne comme contrôleur SCSI d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-109">Occasionally, however, a single device acts as both a network adapter and a controller, for example, when a fiber channel adapter operates as a computer system's SCSI controller.</span></span> <span data-ttu-id="6df7c-110">Dans ce cas, les aspects de l’appareil sont orientés sur le réseau et d’autres sont orientés par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="6df7c-110">In which case, aspects of the device are network oriented and others are controller oriented.</span></span> <span data-ttu-id="6df7c-111">Les classes de contrôleur et d’adaptateur doivent être instanciées et une relation d’identité d’appareil doit également être créée pour lier les différents aspects de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-111">The controller and adapter classes should be instantiated and a device identity relationship should also be created to link the different aspects of the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6df7c-112">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6df7c-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6df7c-113">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6df7c-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6df7c-114">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6df7c-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6df7c-115">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="6df7c-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df7c-116">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6df7c-116">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C532-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_NetworkAdapter : CIM_LogicalDevice
{
  boolean  AutoSense;
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
  uint64   MaxSpeed;
  string   Name;
  string   NetworkAddresses[];
  string   PermanentAddress;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="6df7c-117">Membres</span><span class="sxs-lookup"><span data-stu-id="6df7c-117">Members</span></span>

<span data-ttu-id="6df7c-118">La classe de la carte **CIM \_** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6df7c-118">The **CIM\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="6df7c-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6df7c-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="6df7c-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6df7c-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6df7c-121">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6df7c-121">Methods</span></span>

<span data-ttu-id="6df7c-122">La classe de la carte **CIM \_** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6df7c-122">The **CIM\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="6df7c-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="6df7c-123">Method</span></span>                                                                    | <span data-ttu-id="6df7c-124">Description</span><span class="sxs-lookup"><span data-stu-id="6df7c-124">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6df7c-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="6df7c-125">**Reset**</span></span>](reset-method-in-class-cim-networkadapter.md)                 | <span data-ttu-id="6df7c-126">Demande la réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-126">Requests a reset of the logical device.</span></span> <span data-ttu-id="6df7c-127">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6df7c-127">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6df7c-128">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6df7c-128">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-networkadapter.md) | <span data-ttu-id="6df7c-129">Définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.</span><span class="sxs-lookup"><span data-stu-id="6df7c-129">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6df7c-130">Non implémenté par WMI.</span><span class="sxs-lookup"><span data-stu-id="6df7c-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6df7c-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6df7c-131">Properties</span></span>

<span data-ttu-id="6df7c-132">La classe de la carte **CIM \_** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6df7c-132">The **CIM\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6df7c-133">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="6df7c-133">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6df7c-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-136">Si la **valeur est true**, la carte réseau peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="6df7c-136">If **TRUE**, the network adapter can automatically determine the speed or other communications characteristics of the attached network media.</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-137">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="6df7c-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-138">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6df7c-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6df7c-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-141">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-141">Availability and status of the device.</span></span>

<span data-ttu-id="6df7c-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6df7c-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6df7c-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6df7c-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6df7c-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6df7c-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="6df7c-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6df7c-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="6df7c-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6df7c-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="6df7c-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6df7c-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="6df7c-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6df7c-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="6df7c-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6df7c-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="6df7c-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6df7c-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="6df7c-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6df7c-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="6df7c-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6df7c-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="6df7c-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6df7c-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="6df7c-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6df7c-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="6df7c-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-156">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="6df7c-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6df7c-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="6df7c-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-158">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="6df7c-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6df7c-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="6df7c-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-160">L’appareil ne fonctionne pas mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="6df7c-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6df7c-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="6df7c-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6df7c-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="6df7c-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-163">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6df7c-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6df7c-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="6df7c-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-165">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="6df7c-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6df7c-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="6df7c-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-167">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="6df7c-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6df7c-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="6df7c-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-169">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="6df7c-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6df7c-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="6df7c-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-171">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="6df7c-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6df7c-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6df7c-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-175">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-176">Courte description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6df7c-176">Short textual description of the object.</span></span>

<span data-ttu-id="6df7c-177">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-178">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6df7c-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-179">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6df7c-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-181">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6df7c-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-182">Code d’erreur Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6df7c-182">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="6df7c-183">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6df7c-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6df7c-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="6df7c-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-186">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="6df7c-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6df7c-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6df7c-188">(1)</span><span class="sxs-lookup"><span data-stu-id="6df7c-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-189">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="6df7c-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6df7c-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6df7c-191">(2)</span><span class="sxs-lookup"><span data-stu-id="6df7c-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6df7c-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6df7c-193">(3)</span><span class="sxs-lookup"><span data-stu-id="6df7c-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-194">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="6df7c-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6df7c-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6df7c-196">(4)</span><span class="sxs-lookup"><span data-stu-id="6df7c-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-197">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="6df7c-197">Device is not working properly.</span></span> <span data-ttu-id="6df7c-198">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="6df7c-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6df7c-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6df7c-200">(5)</span><span class="sxs-lookup"><span data-stu-id="6df7c-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-201">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="6df7c-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6df7c-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6df7c-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="6df7c-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-204">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="6df7c-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6df7c-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6df7c-206">(7)</span><span class="sxs-lookup"><span data-stu-id="6df7c-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6df7c-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6df7c-208">(8)</span><span class="sxs-lookup"><span data-stu-id="6df7c-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-209">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="6df7c-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6df7c-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6df7c-211">(9)</span><span class="sxs-lookup"><span data-stu-id="6df7c-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-212">L’appareil ne fonctionne pas correctement ; le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6df7c-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6df7c-214">(10)</span><span class="sxs-lookup"><span data-stu-id="6df7c-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-215">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6df7c-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6df7c-217">(11)</span><span class="sxs-lookup"><span data-stu-id="6df7c-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-218">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6df7c-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6df7c-220">douze</span><span class="sxs-lookup"><span data-stu-id="6df7c-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-221">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6df7c-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6df7c-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6df7c-223">(13)</span><span class="sxs-lookup"><span data-stu-id="6df7c-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-224">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6df7c-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6df7c-226">(14)</span><span class="sxs-lookup"><span data-stu-id="6df7c-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-227">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="6df7c-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6df7c-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6df7c-229">(15)</span><span class="sxs-lookup"><span data-stu-id="6df7c-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-230">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="6df7c-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6df7c-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6df7c-232">(16)</span><span class="sxs-lookup"><span data-stu-id="6df7c-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-233">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6df7c-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6df7c-235">(17)</span><span class="sxs-lookup"><span data-stu-id="6df7c-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-236">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="6df7c-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6df7c-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6df7c-238">(18)</span><span class="sxs-lookup"><span data-stu-id="6df7c-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-239">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="6df7c-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6df7c-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6df7c-241">(19)</span><span class="sxs-lookup"><span data-stu-id="6df7c-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6df7c-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6df7c-243">(20)</span><span class="sxs-lookup"><span data-stu-id="6df7c-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-244">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="6df7c-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6df7c-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6df7c-246">(21)</span><span class="sxs-lookup"><span data-stu-id="6df7c-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-247">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="6df7c-247">System failure.</span></span> <span data-ttu-id="6df7c-248">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="6df7c-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6df7c-249">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6df7c-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6df7c-251">(22)</span><span class="sxs-lookup"><span data-stu-id="6df7c-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-252">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="6df7c-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6df7c-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6df7c-254">(23)</span><span class="sxs-lookup"><span data-stu-id="6df7c-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-255">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="6df7c-255">System failure.</span></span> <span data-ttu-id="6df7c-256">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="6df7c-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6df7c-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6df7c-258">(24)</span><span class="sxs-lookup"><span data-stu-id="6df7c-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-259">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="6df7c-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6df7c-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6df7c-261">(25)</span><span class="sxs-lookup"><span data-stu-id="6df7c-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-262">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6df7c-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6df7c-264">(26)</span><span class="sxs-lookup"><span data-stu-id="6df7c-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-265">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6df7c-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6df7c-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6df7c-267">(27)</span><span class="sxs-lookup"><span data-stu-id="6df7c-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-268">L’appareil n’a pas une configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="6df7c-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6df7c-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6df7c-270">(28)</span><span class="sxs-lookup"><span data-stu-id="6df7c-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-271">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="6df7c-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6df7c-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6df7c-273">(29)</span><span class="sxs-lookup"><span data-stu-id="6df7c-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-274">L’appareil est désactivé ; le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="6df7c-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6df7c-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6df7c-276">(30)</span><span class="sxs-lookup"><span data-stu-id="6df7c-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-277">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="6df7c-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6df7c-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="6df7c-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6df7c-279">31</span><span class="sxs-lookup"><span data-stu-id="6df7c-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-280">L’appareil ne fonctionne pas correctement ; Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="6df7c-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6df7c-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6df7c-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-282">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6df7c-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-284">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6df7c-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-285">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6df7c-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6df7c-286">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6df7c-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-290">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6df7c-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-291">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6df7c-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6df7c-292">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="6df7c-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6df7c-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-294">**Description**</span><span class="sxs-lookup"><span data-stu-id="6df7c-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-297">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6df7c-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-298">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6df7c-298">Textual description of the object.</span></span>

<span data-ttu-id="6df7c-299">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-300">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6df7c-300">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-303">Qualificateurs : [ **\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6df7c-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-304">Adresse ou d’autres informations d’identification pour nommer de manière unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-304">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6df7c-305">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-306">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6df7c-306">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-307">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6df7c-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-309">Si la **valeur est true**, l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="6df7c-309">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6df7c-310">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-311">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6df7c-311">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-314">Chaîne de forme libre qui fournit des informations sur l’erreur enregistrée dans la propriété **LastErrorCode** et les actions correctives à effectuer.</span><span class="sxs-lookup"><span data-stu-id="6df7c-314">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6df7c-315">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-316">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6df7c-316">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-317">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6df7c-317">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-319">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="6df7c-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-320">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6df7c-320">Date and time the object was installed.</span></span> <span data-ttu-id="6df7c-321">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="6df7c-321">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6df7c-322">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-323">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6df7c-323">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-324">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6df7c-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-326">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-326">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6df7c-327">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-328">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="6df7c-328">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-329">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6df7c-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-331">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-332">Vitesse maximale, en bits par seconde (bits/s), pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="6df7c-332">Maximum speed, in bits per second (BPS), for the network adapter.</span></span>

<span data-ttu-id="6df7c-333">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6df7c-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-334">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6df7c-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-337">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6df7c-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-338">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6df7c-338">Label by which the object is known.</span></span> <span data-ttu-id="6df7c-339">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="6df7c-339">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6df7c-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-341">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="6df7c-341">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-342">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="6df7c-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-344">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Carte réseau DMTF 802 Port \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="6df7c-344">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-345">Liste des adresses réseau d’un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="6df7c-345">List of network addresses for an adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-346">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="6df7c-346">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-349">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Carte réseau DMTF 802 Port \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="6df7c-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-350">Adresse réseau codée en dur dans un adaptateur.</span><span class="sxs-lookup"><span data-stu-id="6df7c-350">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="6df7c-351">L’adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="6df7c-351">The hard-coded address can be changed with a firmware upgrade or software configuration.</span></span> <span data-ttu-id="6df7c-352">En cas de modification, le champ doit être mis à jour lorsque la modification est apportée.</span><span class="sxs-lookup"><span data-stu-id="6df7c-352">If changed, the field should be updated when the change is made.</span></span> <span data-ttu-id="6df7c-353">Cette propriété doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="6df7c-353">This property should be left blank if no hard-coded address exists for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-354">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6df7c-354">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-357">Qualificateurs : [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6df7c-357">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-358">Win32 Plug-and-Play identificateur du périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-358">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="6df7c-359">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6df7c-360">Exemple : « \* PNP030b »</span><span class="sxs-lookup"><span data-stu-id="6df7c-360">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-361">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6df7c-361">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-362">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6df7c-362">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-364">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-364">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6df7c-365">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="6df7c-365">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6df7c-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6df7c-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6df7c-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="6df7c-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6df7c-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="6df7c-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6df7c-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6df7c-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-370">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="6df7c-370">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6df7c-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="6df7c-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-372">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="6df7c-372">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6df7c-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="6df7c-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-374">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6df7c-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6df7c-375">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="6df7c-375">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6df7c-376">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6df7c-376">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6df7c-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="6df7c-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-378">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="6df7c-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6df7c-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="6df7c-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6df7c-380">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="6df7c-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6df7c-381">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6df7c-381">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-382">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6df7c-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-384">Si la **valeur est true**, l’appareil peut être géré par le biais de l’alimentation, c’est-à-dire être mis en état d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="6df7c-384">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6df7c-385">Si la valeur est **false**, la valeur entière 1 (« non pris en charge ») doit être la seule entrée dans le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6df7c-385">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6df7c-386">Cette propriété n’indique pas si les fonctionnalités de gestion de l’alimentation sont actuellement activées, ou si elles sont activées, quelles sont les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6df7c-386">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6df7c-387">Pour plus d’informations, consultez le tableau **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6df7c-387">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6df7c-388">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-388">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-389">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="6df7c-389">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-390">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6df7c-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-392">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Carte réseau DMTF 802 Port \| 001,5 "), [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits par seconde ")</span><span class="sxs-lookup"><span data-stu-id="6df7c-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-393">Estimation de la bande passante actuelle, en BPS.</span><span class="sxs-lookup"><span data-stu-id="6df7c-393">Estimate of the current bandwidth, in BPS.</span></span> <span data-ttu-id="6df7c-394">Pour les points de terminaison qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.</span><span class="sxs-lookup"><span data-stu-id="6df7c-394">For endpoints that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="6df7c-395">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6df7c-395">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-396">**État**</span><span class="sxs-lookup"><span data-stu-id="6df7c-396">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-399">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6df7c-399">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-400">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6df7c-400">Current status of the object.</span></span>

<span data-ttu-id="6df7c-401">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6df7c-402">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6df7c-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6df7c-403">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6df7c-404">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6df7c-405">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6df7c-406">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="6df7c-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6df7c-407">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6df7c-408">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6df7c-409">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6df7c-410">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6df7c-411">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6df7c-412">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6df7c-413">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6df7c-414">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="6df7c-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6df7c-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6df7c-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-416">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6df7c-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-418">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6df7c-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-419">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6df7c-419">State of the logical device.</span></span> <span data-ttu-id="6df7c-420">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (non applicable) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6df7c-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6df7c-421">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6df7c-422">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="6df7c-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6df7c-423">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="6df7c-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6df7c-424">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="6df7c-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6df7c-425">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="6df7c-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6df7c-426">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="6df7c-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6df7c-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6df7c-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-430">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6df7c-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-431">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6df7c-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="6df7c-432">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6df7c-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6df7c-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6df7c-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6df7c-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6df7c-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6df7c-436">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6df7c-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6df7c-437">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6df7c-437">Scoping system's name.</span></span>

<span data-ttu-id="6df7c-438">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6df7c-439">Notes</span><span class="sxs-lookup"><span data-stu-id="6df7c-439">Remarks</span></span>

<span data-ttu-id="6df7c-440">La **classe \_ NetworkAdapter CIM** est dérivée [**de \_ CIM LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-440">The **CIM\_NetworkAdapter** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6df7c-441">WMI n’implémente pas cette classe.</span><span class="sxs-lookup"><span data-stu-id="6df7c-441">WMI does not implement this class.</span></span> <span data-ttu-id="6df7c-442">Pour les classes dérivées de la carte **CIM \_**, consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6df7c-442">For classes that are derived from **CIM\_NetworkAdapter**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6df7c-443">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6df7c-443">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6df7c-444">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6df7c-444">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df7c-445">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6df7c-445">Requirements</span></span>



| <span data-ttu-id="6df7c-446">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6df7c-446">Requirement</span></span> | <span data-ttu-id="6df7c-447">Valeur</span><span class="sxs-lookup"><span data-stu-id="6df7c-447">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6df7c-448">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df7c-448">Minimum supported client</span></span><br/> | <span data-ttu-id="6df7c-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6df7c-449">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6df7c-450">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6df7c-450">Minimum supported server</span></span><br/> | <span data-ttu-id="6df7c-451">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6df7c-451">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6df7c-452">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6df7c-452">Namespace</span></span><br/>                | <span data-ttu-id="6df7c-453">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6df7c-453">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6df7c-454">MOF</span><span class="sxs-lookup"><span data-stu-id="6df7c-454">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6df7c-455"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6df7c-455"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6df7c-456">DLL</span><span class="sxs-lookup"><span data-stu-id="6df7c-456">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6df7c-457"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6df7c-457"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df7c-458">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6df7c-458">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df7c-459">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6df7c-459">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

