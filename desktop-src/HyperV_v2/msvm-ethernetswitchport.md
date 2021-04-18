---
description: Représente un port sur le commutateur.
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Msvm_EthernetSwitchPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543002"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="312a7-103">MSVM \_ EthernetSwitchPort, classe</span><span class="sxs-lookup"><span data-stu-id="312a7-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="312a7-104">Représente un port sur le commutateur.</span><span class="sxs-lookup"><span data-stu-id="312a7-104">Represents a port on the switch.</span></span>

<span data-ttu-id="312a7-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="312a7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="312a7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="312a7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="312a7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="312a7-107">Members</span></span>

<span data-ttu-id="312a7-108">La classe **MSVM \_ EthernetSwitchPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="312a7-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="312a7-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="312a7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="312a7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="312a7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="312a7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="312a7-111">Methods</span></span>

<span data-ttu-id="312a7-112">La classe **MSVM \_ EthernetSwitchPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="312a7-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="312a7-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="312a7-113">Method</span></span>                                                                   | <span data-ttu-id="312a7-114">Description</span><span class="sxs-lookup"><span data-stu-id="312a7-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="312a7-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="312a7-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="312a7-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="312a7-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="312a7-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="312a7-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="312a7-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="312a7-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="312a7-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="312a7-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="312a7-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="312a7-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="312a7-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="312a7-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="312a7-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="312a7-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="312a7-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="312a7-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="312a7-124">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="312a7-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="312a7-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="312a7-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="312a7-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="312a7-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="312a7-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="312a7-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="312a7-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="312a7-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="312a7-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="312a7-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="312a7-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="312a7-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="312a7-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="312a7-131">Properties</span></span>

<span data-ttu-id="312a7-132">La classe **MSVM \_ EthernetSwitchPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="312a7-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="312a7-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="312a7-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-134">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-136">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="312a7-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="312a7-137">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="312a7-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="312a7-138">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="312a7-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-140">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-142">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="312a7-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="312a7-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-144">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="312a7-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="312a7-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-147">Indique si le port peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="312a7-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="312a7-148">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-149">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="312a7-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-152">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="312a7-152">The primary availability and status of the device.</span></span> <span data-ttu-id="312a7-153">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="312a7-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-155">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-157">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="312a7-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="312a7-158">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="312a7-159">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="312a7-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="312a7-160">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="312a7-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="312a7-161">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="312a7-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="312a7-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="312a7-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="312a7-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="312a7-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="312a7-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="312a7-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="312a7-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="312a7-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="312a7-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="312a7-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="312a7-172">)</span><span class="sxs-lookup"><span data-stu-id="312a7-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="312a7-173">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="312a7-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-174">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-176">Tableau qui spécifie les fonctionnalités du port.</span><span class="sxs-lookup"><span data-stu-id="312a7-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="312a7-177">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="312a7-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="312a7-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="312a7-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="312a7-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="312a7-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wakeonlan** (3)</span><span class="sxs-lookup"><span data-stu-id="312a7-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Basculement** (4)</span><span class="sxs-lookup"><span data-stu-id="312a7-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="312a7-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="312a7-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="312a7-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-185">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="312a7-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-187">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités de port contenues dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="312a7-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="312a7-188">Chaque entrée de ce tableau est liée à l’entrée correspondante dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="312a7-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="312a7-189">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="312a7-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="312a7-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-193">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="312a7-193">A short description of the object.</span></span> <span data-ttu-id="312a7-194">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et elle est toujours définie sur « port commuté Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="312a7-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="312a7-195">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="312a7-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-198">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="312a7-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="312a7-199">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="312a7-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="312a7-200">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-201">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="312a7-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-204">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="312a7-204">The scoping system's creation class name.</span></span> <span data-ttu-id="312a7-205">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ EthernetSwitchPort ».</span><span class="sxs-lookup"><span data-stu-id="312a7-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="312a7-206">**Description**</span><span class="sxs-lookup"><span data-stu-id="312a7-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-209">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="312a7-209">A description of the object.</span></span> <span data-ttu-id="312a7-210">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port de commutateur Ethernet virtuel Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="312a7-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="312a7-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="312a7-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-214">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="312a7-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="312a7-215">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="312a7-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="312a7-216">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-217">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="312a7-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-220">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="312a7-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="312a7-221">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="312a7-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="312a7-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-225">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="312a7-225">A display name for the object.</span></span> <span data-ttu-id="312a7-226">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-227">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="312a7-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-228">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-230">Spécifie les fonctionnalités qui sont activées dans la liste de toutes les fonctionnalités prises en charge dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="312a7-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="312a7-231">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="312a7-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="312a7-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="312a7-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="312a7-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="312a7-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wakeonlan** (3)</span><span class="sxs-lookup"><span data-stu-id="312a7-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Basculement** (4)</span><span class="sxs-lookup"><span data-stu-id="312a7-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="312a7-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="312a7-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="312a7-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-239">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-241">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="312a7-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="312a7-242">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="312a7-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="312a7-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-246">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="312a7-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="312a7-247">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="312a7-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="312a7-248">Valeur</span><span class="sxs-lookup"><span data-stu-id="312a7-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="312a7-249">Signification</span><span class="sxs-lookup"><span data-stu-id="312a7-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="312a7-250"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="312a7-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="312a7-251">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="312a7-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="312a7-252"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="312a7-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="312a7-253">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="312a7-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="312a7-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="312a7-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-255">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="312a7-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-257">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="312a7-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="312a7-258">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="312a7-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-262">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="312a7-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="312a7-263">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-264">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="312a7-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-265">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="312a7-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-267">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="312a7-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="312a7-268">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="312a7-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-270">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-272">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="312a7-272">The current health of the element.</span></span> <span data-ttu-id="312a7-273">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="312a7-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="312a7-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-275">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="312a7-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-277">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="312a7-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="312a7-278">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="312a7-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-280">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="312a7-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-282">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="312a7-282">The date and time when the object was installed.</span></span> <span data-ttu-id="312a7-283">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="312a7-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="312a7-284">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="312a7-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-288">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="312a7-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="312a7-289">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="312a7-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="312a7-290">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-291">**IOVOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="312a7-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-292">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="312a7-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-294">Utilisation du déchargement de la virtualisation d’e/s en cours sur ce port.</span><span class="sxs-lookup"><span data-stu-id="312a7-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="312a7-295">L’utilisation correspond à la quantité de ressources IOV en cours d’utilisation sur le port.</span><span class="sxs-lookup"><span data-stu-id="312a7-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-296">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="312a7-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-297">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="312a7-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-299">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="312a7-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="312a7-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-301">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="312a7-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-302">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-304">Spécifie le type de technologie de lien pour le port.</span><span class="sxs-lookup"><span data-stu-id="312a7-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="312a7-305">Lorsque la valeur 1 (autre) est définie, la propriété **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="312a7-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="312a7-306">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="312a7-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="312a7-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="312a7-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="312a7-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="312a7-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="312a7-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="312a7-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="312a7-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="312a7-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Relais de trames** (8)</span><span class="sxs-lookup"><span data-stu-id="312a7-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarouge** (9)</span><span class="sxs-lookup"><span data-stu-id="312a7-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="312a7-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Réseau local sans fil** (11)</span><span class="sxs-lookup"><span data-stu-id="312a7-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="312a7-319">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="312a7-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-320">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="312a7-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-322">Taille maximale du champ INFO (non-MAC) qui sera reçu ou transmis.</span><span class="sxs-lookup"><span data-stu-id="312a7-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="312a7-323">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et est toujours définie sur 1500.</span><span class="sxs-lookup"><span data-stu-id="312a7-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-324">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="312a7-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-325">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-327">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="312a7-327">This property has been deprecated.</span></span> <span data-ttu-id="312a7-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-329">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="312a7-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-330">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-332">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="312a7-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="312a7-333">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="312a7-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="312a7-334">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-335">**Nom**</span><span class="sxs-lookup"><span data-stu-id="312a7-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-338">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="312a7-338">The label by which the object is known.</span></span> <span data-ttu-id="312a7-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-340">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="312a7-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-341">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="312a7-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-343">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="312a7-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="312a7-344">Tableau de chaînes qui contient les adresses MAC du port.</span><span class="sxs-lookup"><span data-stu-id="312a7-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="312a7-345">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-346">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="312a7-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-347">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-349">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="312a7-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="312a7-350">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="312a7-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="312a7-351">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="312a7-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-353">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-355">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="312a7-355">The current statuses of the object.</span></span> <span data-ttu-id="312a7-356">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="312a7-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-357">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="312a7-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-358">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="312a7-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-360">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités activées spécifiées comme 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="312a7-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="312a7-361">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="312a7-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="312a7-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-363">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-365">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="312a7-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="312a7-366">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="312a7-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="312a7-367">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="312a7-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="312a7-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-369">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="312a7-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-371">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="312a7-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="312a7-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-373">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="312a7-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-376">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1, (other).</span><span class="sxs-lookup"><span data-stu-id="312a7-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="312a7-377">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-378">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="312a7-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-381">L’utilisation de cette propriété est déconseillée à la place de la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="312a7-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="312a7-382">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-383">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="312a7-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-384">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-386">Décrit le type de module, lorsque **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="312a7-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="312a7-387">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-388">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="312a7-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-389">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-391">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="312a7-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="312a7-392">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="312a7-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="312a7-393">Cette adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="312a7-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="312a7-394">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="312a7-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="312a7-395">Cette propriété doit avoir la **valeur null** s’il n’existe aucune adresse codée en dur pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="312a7-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="312a7-396">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-397">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="312a7-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-398">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-400">Le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="312a7-400">The port number.</span></span> <span data-ttu-id="312a7-401">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-402">**PortType**</span><span class="sxs-lookup"><span data-stu-id="312a7-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-403">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-405">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="312a7-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="312a7-406">Si la valeur 1 (autre) est définie, la propriété **OtherPortType** associée contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="312a7-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="312a7-407">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="312a7-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="312a7-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="312a7-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cuivre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="312a7-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="312a7-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="312a7-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="312a7-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="312a7-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="312a7-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="312a7-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="312a7-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="312a7-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="312a7-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="312a7-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="312a7-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="312a7-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="312a7-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="312a7-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="312a7-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="312a7-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="312a7-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-SEM** (111)</span><span class="sxs-lookup"><span data-stu-id="312a7-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="312a7-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="312a7-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="312a7-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-431">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-433">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="312a7-433">The power management capabilities of the device.</span></span> <span data-ttu-id="312a7-434">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="312a7-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-436">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="312a7-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-438">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="312a7-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="312a7-439">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-440">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="312a7-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-441">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-443">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="312a7-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="312a7-444">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-445">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="312a7-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-446">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-448">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="312a7-448">Provides high level status information.</span></span> <span data-ttu-id="312a7-449">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="312a7-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="312a7-450">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="312a7-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="312a7-451">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-452">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="312a7-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-453">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-454">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-455">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="312a7-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="312a7-456">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="312a7-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="312a7-457">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="312a7-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="312a7-458">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="312a7-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-460">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-461">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-462">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="312a7-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="312a7-463">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="312a7-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-464">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="312a7-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-465">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-467">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="312a7-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="312a7-468">La bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="312a7-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="312a7-469">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-470">**État**</span><span class="sxs-lookup"><span data-stu-id="312a7-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-471">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-473">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="312a7-473">The current status of the object.</span></span> <span data-ttu-id="312a7-474">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-475">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="312a7-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-476">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="312a7-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="312a7-477">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-478">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="312a7-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="312a7-479">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="312a7-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="312a7-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-481">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-483">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="312a7-483">The current state of the logical device.</span></span> <span data-ttu-id="312a7-484">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-485">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="312a7-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-486">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="312a7-488">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="312a7-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="312a7-489">Unité de transmission maximale (MTU) qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="312a7-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="312a7-490">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="312a7-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="312a7-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-492">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-494">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="312a7-494">The scoping system's creation class name.</span></span> <span data-ttu-id="312a7-495">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ VirtualEthernetSwitch ».</span><span class="sxs-lookup"><span data-stu-id="312a7-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="312a7-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="312a7-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-497">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="312a7-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-498">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-499">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="312a7-499">The scoping system's name.</span></span> <span data-ttu-id="312a7-500">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="312a7-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="312a7-501">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="312a7-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-502">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="312a7-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-504">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="312a7-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="312a7-505">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="312a7-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-506">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="312a7-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-507">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="312a7-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-508">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-509">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="312a7-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="312a7-510">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-511">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="312a7-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-512">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-513">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-514">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="312a7-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="312a7-515">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="312a7-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="312a7-516">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="312a7-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-517">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="312a7-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-518">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-519">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="312a7-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="312a7-520">C’est le cas, par exemple, d’un groupe de stockage qui peut avoir back end ports pour communiquer avec les lecteurs de disque et les ports frontaux pour communiquer avec les hôtes.</span><span class="sxs-lookup"><span data-stu-id="312a7-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="312a7-521">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (non limité).</span><span class="sxs-lookup"><span data-stu-id="312a7-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="312a7-522">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="312a7-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="312a7-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="312a7-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Frontal uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="312a7-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Serveur principal uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="312a7-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="312a7-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Non restreint** (4)</span><span class="sxs-lookup"><span data-stu-id="312a7-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="312a7-527">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="312a7-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="312a7-528">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="312a7-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="312a7-529">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="312a7-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="312a7-530">La file d’attente d’ordinateurs virtuels actuelle déchargement de l’utilisation sur ce port.</span><span class="sxs-lookup"><span data-stu-id="312a7-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="312a7-531">L’utilisation correspond à la quantité de ressources d’ordinateurs virtuels en cours d’utilisation sur le port.</span><span class="sxs-lookup"><span data-stu-id="312a7-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="312a7-532">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="312a7-532">Requirements</span></span>



| <span data-ttu-id="312a7-533">Condition requise</span><span class="sxs-lookup"><span data-stu-id="312a7-533">Requirement</span></span> | <span data-ttu-id="312a7-534">Valeur</span><span class="sxs-lookup"><span data-stu-id="312a7-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="312a7-535">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="312a7-535">Minimum supported client</span></span><br/> | <span data-ttu-id="312a7-536">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="312a7-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="312a7-537">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="312a7-537">Minimum supported server</span></span><br/> | <span data-ttu-id="312a7-538">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="312a7-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="312a7-539">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="312a7-539">Namespace</span></span><br/>                | <span data-ttu-id="312a7-540">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="312a7-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="312a7-541">MOF</span><span class="sxs-lookup"><span data-stu-id="312a7-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="312a7-542"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="312a7-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="312a7-543">DLL</span><span class="sxs-lookup"><span data-stu-id="312a7-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="312a7-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="312a7-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

