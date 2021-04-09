---
description: Représente une carte réseau Wi-Fi physique (802,11) qui peut être liée à un commutateur virtuel pour fournir une connectivité réseau externe aux ordinateurs virtuels.
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Msvm_WiFiPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953180"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="22f24-103">MSVM \_ WiFiPort, classe</span><span class="sxs-lookup"><span data-stu-id="22f24-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="22f24-104">Représente une carte réseau Wi-Fi physique (802,11) qui peut être liée à un commutateur virtuel pour fournir une connectivité réseau externe aux ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="22f24-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="22f24-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="22f24-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f24-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22f24-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="22f24-107">Membres</span><span class="sxs-lookup"><span data-stu-id="22f24-107">Members</span></span>

<span data-ttu-id="22f24-108">La classe **MSVM \_ WiFiPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="22f24-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="22f24-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="22f24-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="22f24-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="22f24-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22f24-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="22f24-111">Methods</span></span>

<span data-ttu-id="22f24-112">La classe **MSVM \_ WiFiPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="22f24-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="22f24-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="22f24-113">Method</span></span>                 | <span data-ttu-id="22f24-114">Description</span><span class="sxs-lookup"><span data-stu-id="22f24-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="22f24-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="22f24-115">**EnableDevice**</span></span>       | <span data-ttu-id="22f24-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="22f24-117">**OnlineDevice**</span></span>       | <span data-ttu-id="22f24-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="22f24-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="22f24-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="22f24-121">**RequestStateChange**</span></span> | <span data-ttu-id="22f24-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="22f24-123">**Reset**</span></span>              | <span data-ttu-id="22f24-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="22f24-125">**RestoreProperties**</span></span>  | <span data-ttu-id="22f24-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="22f24-127">**SaveProperties**</span></span>     | <span data-ttu-id="22f24-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="22f24-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="22f24-129">**SetPowerState**</span></span>      | <span data-ttu-id="22f24-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22f24-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22f24-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="22f24-131">Properties</span></span>

<span data-ttu-id="22f24-132">La classe **MSVM \_ WiFiPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="22f24-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22f24-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="22f24-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-134">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-136">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22f24-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22f24-137">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="22f24-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="22f24-138">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="22f24-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-140">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-142">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="22f24-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="22f24-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-144">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="22f24-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22f24-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-147">Indique si le port peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="22f24-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="22f24-148">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-149">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="22f24-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-150">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-152">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="22f24-152">The primary availability and status of the device.</span></span> <span data-ttu-id="22f24-153">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="22f24-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-155">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-157">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="22f24-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="22f24-158">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="22f24-159">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="22f24-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="22f24-160">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="22f24-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="22f24-161">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="22f24-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="22f24-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="22f24-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="22f24-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="22f24-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="22f24-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="22f24-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="22f24-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="22f24-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="22f24-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="22f24-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="22f24-172">)</span><span class="sxs-lookup"><span data-stu-id="22f24-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22f24-173">**Caption**</span><span class="sxs-lookup"><span data-stu-id="22f24-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-176">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="22f24-176">A short description of the object.</span></span> <span data-ttu-id="22f24-177">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="22f24-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="22f24-178">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="22f24-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-179">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-181">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="22f24-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="22f24-182">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="22f24-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f24-183">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22f24-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-187">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="22f24-187">The scoping system's creation class name.</span></span> <span data-ttu-id="22f24-188">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-189">**Description**</span><span class="sxs-lookup"><span data-stu-id="22f24-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-192">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="22f24-192">A description of the object.</span></span> <span data-ttu-id="22f24-193">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="22f24-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-195">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-197">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="22f24-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="22f24-198">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="22f24-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f24-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-200">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="22f24-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-203">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="22f24-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="22f24-204">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22f24-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-208">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="22f24-208">A display name for the object.</span></span> <span data-ttu-id="22f24-209">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="22f24-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-213">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="22f24-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="22f24-214">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="22f24-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-216">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-218">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="22f24-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="22f24-219">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="22f24-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="22f24-220">Valeur</span><span class="sxs-lookup"><span data-stu-id="22f24-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="22f24-221">Signification</span><span class="sxs-lookup"><span data-stu-id="22f24-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="22f24-222"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22f24-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="22f24-223">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22f24-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="22f24-224"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="22f24-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="22f24-225">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="22f24-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22f24-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="22f24-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-227">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22f24-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-229">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="22f24-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="22f24-230">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="22f24-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-234">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="22f24-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="22f24-235">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-236">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="22f24-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-237">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22f24-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-239">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="22f24-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="22f24-240">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="22f24-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-242">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-244">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="22f24-244">The current health of the element.</span></span> <span data-ttu-id="22f24-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22f24-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-247">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="22f24-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-249">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="22f24-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="22f24-250">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22f24-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-252">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22f24-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-254">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="22f24-254">The date and time when the object was installed.</span></span> <span data-ttu-id="22f24-255">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="22f24-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="22f24-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22f24-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-260">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="22f24-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22f24-261">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="22f24-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22f24-262">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-263">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="22f24-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-264">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22f24-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-266">Spécifie si le port Wi-Fi est lié à l’architecture réseau de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="22f24-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="22f24-267">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="22f24-267">This will be one of the following values.</span></span>



| <span data-ttu-id="22f24-268">Valeur</span><span class="sxs-lookup"><span data-stu-id="22f24-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="22f24-269">Signification</span><span class="sxs-lookup"><span data-stu-id="22f24-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="22f24-270"><dt>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="22f24-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="22f24-271">Le port Wi-Fi est lié à l’architecture réseau de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="22f24-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="22f24-272"><dt>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="22f24-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="22f24-273">Le port Wi-Fi n’est pas lié à l’architecture réseau de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="22f24-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="22f24-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22f24-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-275">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22f24-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-277">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="22f24-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="22f24-278">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-279">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="22f24-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-280">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-282">Spécifie le type de technologie de lien pour le port.</span><span class="sxs-lookup"><span data-stu-id="22f24-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="22f24-283">Lorsque la valeur 1 (autre) est définie, la propriété **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="22f24-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="22f24-284">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="22f24-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="22f24-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="22f24-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="22f24-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="22f24-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="22f24-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="22f24-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="22f24-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="22f24-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Relais de trames** (8)</span><span class="sxs-lookup"><span data-stu-id="22f24-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarouge** (9)</span><span class="sxs-lookup"><span data-stu-id="22f24-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="22f24-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Réseau local sans fil** (11)</span><span class="sxs-lookup"><span data-stu-id="22f24-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22f24-297">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="22f24-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-298">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-300">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="22f24-300">This property has been deprecated.</span></span> <span data-ttu-id="22f24-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-302">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="22f24-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-303">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-305">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="22f24-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="22f24-306">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="22f24-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="22f24-307">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-308">**Nom**</span><span class="sxs-lookup"><span data-stu-id="22f24-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-311">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="22f24-311">The label by which the object is known.</span></span> <span data-ttu-id="22f24-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-313">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="22f24-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-314">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="22f24-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-316">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="22f24-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="22f24-317">Tableau de chaînes qui contient les adresses MAC du port.</span><span class="sxs-lookup"><span data-stu-id="22f24-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="22f24-318">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-319">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="22f24-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-320">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-322">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="22f24-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="22f24-323">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="22f24-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f24-324">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="22f24-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-326">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-328">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="22f24-328">The current statuses of the object.</span></span> <span data-ttu-id="22f24-329">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-330">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="22f24-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-333">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="22f24-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="22f24-334">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="22f24-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="22f24-335">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="22f24-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-337">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="22f24-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-339">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="22f24-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="22f24-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="22f24-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-344">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1, (other).</span><span class="sxs-lookup"><span data-stu-id="22f24-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="22f24-345">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="22f24-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-349">L’utilisation de cette propriété est déconseillée à la place de la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="22f24-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="22f24-350">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-351">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="22f24-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-354">Décrit le type de module, lorsque **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="22f24-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="22f24-355">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-356">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="22f24-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-357">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-359">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="22f24-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="22f24-360">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="22f24-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="22f24-361">Cette adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="22f24-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="22f24-362">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="22f24-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="22f24-363">Cette propriété doit avoir la **valeur null** s’il n’existe aucune adresse codée en dur pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="22f24-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="22f24-364">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-365">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="22f24-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-366">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-368">Le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="22f24-368">The port number.</span></span> <span data-ttu-id="22f24-369">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-370">**PortType**</span><span class="sxs-lookup"><span data-stu-id="22f24-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-371">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-373">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="22f24-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="22f24-374">Si la valeur 1 (autre) est définie, la propriété **OtherPortType** associée contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="22f24-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="22f24-375">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="22f24-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="22f24-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="22f24-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cuivre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="22f24-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="22f24-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="22f24-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="22f24-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="22f24-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="22f24-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="22f24-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="22f24-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="22f24-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="22f24-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="22f24-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="22f24-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="22f24-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="22f24-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="22f24-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="22f24-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="22f24-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="22f24-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-SEM** (111)</span><span class="sxs-lookup"><span data-stu-id="22f24-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="22f24-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="22f24-398">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="22f24-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-399">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-401">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="22f24-401">The power management capabilities of the device.</span></span> <span data-ttu-id="22f24-402">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-403">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="22f24-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-404">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="22f24-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-406">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="22f24-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="22f24-407">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-408">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="22f24-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-409">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-411">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="22f24-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="22f24-412">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-413">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="22f24-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-414">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-416">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="22f24-416">Provides high level status information.</span></span> <span data-ttu-id="22f24-417">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="22f24-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="22f24-418">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="22f24-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="22f24-419">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-420">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="22f24-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-421">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-422">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-423">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="22f24-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="22f24-424">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="22f24-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="22f24-425">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="22f24-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="22f24-426">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="22f24-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-428">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-430">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="22f24-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="22f24-431">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-432">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="22f24-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-433">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-435">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="22f24-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="22f24-436">La bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="22f24-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="22f24-437">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-438">**État**</span><span class="sxs-lookup"><span data-stu-id="22f24-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-441">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="22f24-441">The current status of the object.</span></span> <span data-ttu-id="22f24-442">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-443">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="22f24-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-444">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="22f24-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22f24-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-446">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="22f24-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="22f24-447">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="22f24-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="22f24-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-449">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-451">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="22f24-451">The current state of the logical device.</span></span> <span data-ttu-id="22f24-452">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-453">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="22f24-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-454">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22f24-456">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="22f24-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="22f24-457">Unité de transmission maximale (MTU) qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="22f24-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="22f24-458">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="22f24-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-459">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22f24-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-460">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-461">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-462">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="22f24-462">The scoping system's creation class name.</span></span> <span data-ttu-id="22f24-463">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="22f24-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-465">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22f24-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-466">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-467">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="22f24-467">The scoping system's name.</span></span> <span data-ttu-id="22f24-468">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-469">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="22f24-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-470">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22f24-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-471">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-472">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="22f24-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="22f24-473">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-474">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="22f24-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-475">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="22f24-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-477">Nombre total d’heures de mise sous tension de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="22f24-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="22f24-478">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="22f24-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="22f24-479">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="22f24-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-480">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-482">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="22f24-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="22f24-483">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="22f24-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22f24-484">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="22f24-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22f24-485">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22f24-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22f24-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="22f24-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22f24-487">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="22f24-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="22f24-488">C’est le cas, par exemple, d’un groupe de stockage qui peut avoir back end ports pour communiquer avec les lecteurs de disque et les ports frontaux pour communiquer avec les hôtes.</span><span class="sxs-lookup"><span data-stu-id="22f24-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="22f24-489">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (non limité).</span><span class="sxs-lookup"><span data-stu-id="22f24-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="22f24-490">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="22f24-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="22f24-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="22f24-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Frontal uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="22f24-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Serveur principal uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="22f24-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="22f24-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Non restreint** (4)</span><span class="sxs-lookup"><span data-stu-id="22f24-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22f24-495">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22f24-495">Requirements</span></span>



| <span data-ttu-id="22f24-496">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22f24-496">Requirement</span></span> | <span data-ttu-id="22f24-497">Valeur</span><span class="sxs-lookup"><span data-stu-id="22f24-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22f24-498">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22f24-498">Minimum supported client</span></span><br/> | <span data-ttu-id="22f24-499">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22f24-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22f24-500">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22f24-500">Minimum supported server</span></span><br/> | <span data-ttu-id="22f24-501">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22f24-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22f24-502">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="22f24-502">Namespace</span></span><br/>                | <span data-ttu-id="22f24-503">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="22f24-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22f24-504">MOF</span><span class="sxs-lookup"><span data-stu-id="22f24-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22f24-505"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22f24-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22f24-506">DLL</span><span class="sxs-lookup"><span data-stu-id="22f24-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22f24-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22f24-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

