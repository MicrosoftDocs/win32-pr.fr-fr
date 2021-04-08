---
description: Représente une carte Ethernet synthétique.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Msvm_SyntheticEthernetPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863874"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="59851-103">MSVM \_ SyntheticEthernetPort, classe</span><span class="sxs-lookup"><span data-stu-id="59851-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="59851-104">Représente une carte Ethernet synthétique.</span><span class="sxs-lookup"><span data-stu-id="59851-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="59851-105">Il s’agit de la carte réseau préférée en raison de ses performances et du fait que les modifications apportées peuvent prendre effet immédiatement, alors qu’elle est en cours d’utilisation (configurable à chaud).</span><span class="sxs-lookup"><span data-stu-id="59851-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="59851-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="59851-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59851-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59851-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="59851-108">Membres</span><span class="sxs-lookup"><span data-stu-id="59851-108">Members</span></span>

<span data-ttu-id="59851-109">La classe **MSVM \_ SyntheticEthernetPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="59851-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="59851-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="59851-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="59851-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59851-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="59851-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="59851-112">Methods</span></span>

<span data-ttu-id="59851-113">La classe **MSVM \_ SyntheticEthernetPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="59851-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="59851-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="59851-114">Method</span></span>                                                                      | <span data-ttu-id="59851-115">Description</span><span class="sxs-lookup"><span data-stu-id="59851-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="59851-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="59851-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="59851-117">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="59851-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="59851-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="59851-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="59851-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="59851-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="59851-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="59851-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="59851-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="59851-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="59851-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="59851-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="59851-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="59851-125">Réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="59851-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="59851-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="59851-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="59851-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="59851-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="59851-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="59851-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="59851-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="59851-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="59851-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="59851-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="59851-132">Properties</span></span>

<span data-ttu-id="59851-133">La classe **MSVM \_ SyntheticEthernetPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="59851-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="59851-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="59851-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59851-137">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="59851-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="59851-138">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="59851-139">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="59851-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-141">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-143">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="59851-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="59851-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="59851-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="59851-145">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="59851-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="59851-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59851-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-148">Indique si le port réseau peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="59851-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="59851-149">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-150">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="59851-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-153">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="59851-153">The primary availability and status of the device.</span></span> <span data-ttu-id="59851-154">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="59851-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="59851-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="59851-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-156">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-158">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="59851-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="59851-159">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="59851-160">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="59851-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="59851-161">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="59851-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="59851-162">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="59851-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="59851-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="59851-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="59851-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="59851-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="59851-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="59851-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="59851-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="59851-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="59851-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="59851-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="59851-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="59851-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="59851-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="59851-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="59851-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="59851-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="59851-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="59851-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="59851-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="59851-173">)</span><span class="sxs-lookup"><span data-stu-id="59851-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59851-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="59851-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-175">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-177">Les fonctionnalités du port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="59851-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="59851-178">Par exemple, l’appareil peut prendre en charge AlertOnLan, WakeOnLan, l’équilibrage de charge ou le basculement.</span><span class="sxs-lookup"><span data-stu-id="59851-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="59851-179">Si les fonctionnalités de basculement ou d’équilibrage de charge sont répertoriées, un SpareGroup (basculement) ou un ExtraCapacityGroup (équilibrage de charge) doit également être défini pour décrire complètement la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="59851-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="59851-180">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-181">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="59851-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-182">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="59851-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-184">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités EthernetPort indiquées dans le tableau de propriétés **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="59851-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="59851-185">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés **Capabilities** situé dans le même index.</span><span class="sxs-lookup"><span data-stu-id="59851-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="59851-186">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-187">**Caption**</span><span class="sxs-lookup"><span data-stu-id="59851-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-190">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="59851-190">A short description of the object.</span></span> <span data-ttu-id="59851-191">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="59851-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-192">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="59851-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-193">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-195">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="59851-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="59851-196">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="59851-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="59851-197">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="59851-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-201">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="59851-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="59851-202">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="59851-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="59851-203">**Description**</span><span class="sxs-lookup"><span data-stu-id="59851-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-206">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="59851-206">A description of the object.</span></span> <span data-ttu-id="59851-207">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="59851-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="59851-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-209">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-211">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="59851-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="59851-212">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="59851-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="59851-213">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="59851-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-217">Une adresse ou d’autres informations d’identification utilisées pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="59851-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="59851-218">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="59851-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="59851-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="59851-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-222">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="59851-222">A display name for the object.</span></span> <span data-ttu-id="59851-223">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="59851-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-224">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="59851-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-225">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-227">Les fonctionnalités qui sont activées dans la liste de tous les types pris en charge, qui sont définies dans le tableau de propriétés **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="59851-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="59851-228">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-229">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="59851-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-230">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-232">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="59851-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="59851-233">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="59851-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-235">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-237">États activés et désactivés de cet élément.</span><span class="sxs-lookup"><span data-stu-id="59851-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="59851-238">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-239">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="59851-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-240">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="59851-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59851-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-242">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="59851-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-246">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-247">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="59851-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-248">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="59851-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59851-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-250">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="59851-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="59851-251">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="59851-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-253">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-255">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="59851-255">The current health of the element.</span></span> <span data-ttu-id="59851-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="59851-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-258">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="59851-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-260">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="59851-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="59851-261">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="59851-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-263">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="59851-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59851-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-265">Date à laquelle le port Ethernet a été ajouté à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="59851-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="59851-266">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="59851-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59851-270">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="59851-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="59851-271">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="59851-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="59851-272">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="59851-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="59851-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-274">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59851-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59851-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-276">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-277">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="59851-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-278">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-280">Énumération des types de liens.</span><span class="sxs-lookup"><span data-stu-id="59851-280">An enumeration of the types of links.</span></span> <span data-ttu-id="59851-281">Si la valeur 1 (autre) est définie, la propriété associée **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="59851-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="59851-282">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="59851-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="59851-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59851-284">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="59851-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="59851-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="59851-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-287">Taille maximale du champ INFO (non-MAC) qui sera reçu ou transmis.</span><span class="sxs-lookup"><span data-stu-id="59851-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="59851-288">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="59851-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-289">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="59851-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-290">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-292">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-293">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="59851-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-294">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59851-296">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="59851-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="59851-297">Bande passante maximale du port en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="59851-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="59851-298">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-299">**Nom**</span><span class="sxs-lookup"><span data-stu-id="59851-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-302">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="59851-302">A display name for the object.</span></span> <span data-ttu-id="59851-303">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="59851-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="59851-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-305">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="59851-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-307">Adresses MAC Ethernet/802.3 au format 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques (le bit d’adresse de groupe se trouve dans le bit de poids faible du premier caractère de la chaîne).</span><span class="sxs-lookup"><span data-stu-id="59851-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="59851-308">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-309">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="59851-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-310">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-312">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="59851-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="59851-313">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="59851-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="59851-314">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="59851-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-316">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-318">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="59851-318">The current status of the element.</span></span> <span data-ttu-id="59851-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="59851-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="59851-320">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="59851-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-321">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="59851-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-323">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités activées spécifiées comme « other ».</span><span class="sxs-lookup"><span data-stu-id="59851-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="59851-324">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-325">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="59851-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-326">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-328">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="59851-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="59851-329">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="59851-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-331">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="59851-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-333">Toutes les données, en plus des informations d’ID de l’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="59851-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="59851-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-335">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="59851-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-338">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="59851-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="59851-339">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-340">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="59851-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-343">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="59851-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="59851-344">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="59851-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-347">Type de module, lorsque **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="59851-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="59851-348">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-349">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="59851-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-352">Adresse réseau qui est codée en dur dans le port.</span><span class="sxs-lookup"><span data-stu-id="59851-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="59851-353">Cette adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="59851-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="59851-354">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="59851-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="59851-355">La propriété **PermanentAddress** doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="59851-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="59851-356">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-357">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="59851-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-358">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-360">Les ports réseau sont souvent numérotés par rapport à un module logique ou à un élément réseau.</span><span class="sxs-lookup"><span data-stu-id="59851-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="59851-361">Cette valeur est 1 pour les cartes réseau émulées, 0 pour toutes les autres.</span><span class="sxs-lookup"><span data-stu-id="59851-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="59851-362">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="59851-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-364">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-366">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="59851-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="59851-367">Si la valeur 1 (autre) est définie, la propriété associée **OtherPortType** contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="59851-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="59851-368">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="59851-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="59851-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-370">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-373">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="59851-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-374">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="59851-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="59851-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-376">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-377">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="59851-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-378">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-380">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-381">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="59851-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-382">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-384">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="59851-384">Provides high level status information.</span></span> <span data-ttu-id="59851-385">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="59851-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="59851-386">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="59851-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="59851-387">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="59851-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-389">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59851-391">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="59851-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="59851-392">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="59851-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="59851-393">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="59851-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="59851-394">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="59851-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-396">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-398">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="59851-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="59851-399">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-400">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="59851-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-401">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59851-403">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="59851-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="59851-404">Bande passante actuelle du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="59851-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="59851-405">Pour les ports qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.</span><span class="sxs-lookup"><span data-stu-id="59851-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="59851-406">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-407">**État**</span><span class="sxs-lookup"><span data-stu-id="59851-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-408">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-410">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="59851-410">The current status of the element.</span></span> <span data-ttu-id="59851-411">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-412">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="59851-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-413">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="59851-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="59851-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-415">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="59851-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="59851-416">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="59851-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="59851-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="59851-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-418">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-420">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-421">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="59851-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-422">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59851-424">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="59851-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="59851-425">Unité de transmission maximale (MTU) qui peut être prise en charge.</span><span class="sxs-lookup"><span data-stu-id="59851-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="59851-426">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="59851-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="59851-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="59851-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-430">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="59851-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="59851-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="59851-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="59851-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="59851-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="59851-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59851-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-435">Nom NetBIOS du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="59851-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="59851-436">Cette propriété contient l’ID de machine virtuelle sous forme de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="59851-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="59851-437">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="59851-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="59851-438">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="59851-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-439">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="59851-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="59851-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-441">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="59851-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="59851-442">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-443">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="59851-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-444">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="59851-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="59851-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-446">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="59851-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="59851-447">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="59851-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-448">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-450">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="59851-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="59851-451">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="59851-452">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="59851-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59851-453">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="59851-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="59851-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="59851-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="59851-455">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="59851-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="59851-456">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (non limité).</span><span class="sxs-lookup"><span data-stu-id="59851-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="59851-457">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59851-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59851-458">Notes</span><span class="sxs-lookup"><span data-stu-id="59851-458">Remarks</span></span>

<span data-ttu-id="59851-459">L’accès à la classe **MSVM \_ SyntheticEthernetPort** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="59851-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="59851-460">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="59851-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="59851-461">Exemples</span><span class="sxs-lookup"><span data-stu-id="59851-461">Examples</span></span>

<span data-ttu-id="59851-462">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="59851-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59851-463">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59851-463">Requirements</span></span>



| <span data-ttu-id="59851-464">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59851-464">Requirement</span></span> | <span data-ttu-id="59851-465">Valeur</span><span class="sxs-lookup"><span data-stu-id="59851-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59851-466">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59851-466">Minimum supported client</span></span><br/> | <span data-ttu-id="59851-467">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59851-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="59851-468">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59851-468">Minimum supported server</span></span><br/> | <span data-ttu-id="59851-469">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59851-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59851-470">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="59851-470">Namespace</span></span><br/>                | <span data-ttu-id="59851-471">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="59851-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="59851-472">MOF</span><span class="sxs-lookup"><span data-stu-id="59851-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59851-473"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59851-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59851-474">DLL</span><span class="sxs-lookup"><span data-stu-id="59851-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59851-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59851-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59851-476">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59851-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59851-477">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="59851-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="59851-478">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="59851-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

