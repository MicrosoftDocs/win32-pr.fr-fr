---
description: Représente un port Ethernet interne (carte réseau).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Msvm_InternalEthernetPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752365"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="df950-103">MSVM \_ InternalEthernetPort, classe</span><span class="sxs-lookup"><span data-stu-id="df950-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="df950-104">Représente un port Ethernet interne (carte réseau).</span><span class="sxs-lookup"><span data-stu-id="df950-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="df950-105">Ce type de port Ethernet permet aux ordinateurs virtuels d’accéder au serveur de virtualisation exécutant le logiciel de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="df950-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="df950-106">Les cartes réseau internes permettent au trafic réseau des ordinateurs virtuels d’être acheminés ou filtrés avant de quitter le système physique.</span><span class="sxs-lookup"><span data-stu-id="df950-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="df950-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="df950-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df950-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df950-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_InternalEthernetPort";
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
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="df950-109">Membres</span><span class="sxs-lookup"><span data-stu-id="df950-109">Members</span></span>

<span data-ttu-id="df950-110">La classe **MSVM \_ InternalEthernetPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="df950-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="df950-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df950-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="df950-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df950-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df950-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="df950-113">Methods</span></span>

<span data-ttu-id="df950-114">La classe **MSVM \_ InternalEthernetPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="df950-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="df950-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="df950-115">Method</span></span>                                                                     | <span data-ttu-id="df950-116">Description</span><span class="sxs-lookup"><span data-stu-id="df950-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="df950-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="df950-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="df950-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df950-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="df950-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="df950-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df950-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="df950-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="df950-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="df950-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="df950-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="df950-124">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="df950-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="df950-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="df950-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="df950-126">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="df950-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="df950-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="df950-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="df950-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df950-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="df950-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="df950-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df950-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="df950-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="df950-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df950-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="df950-133">Properties</span></span>

<span data-ttu-id="df950-134">La classe **MSVM \_ InternalEthernetPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="df950-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df950-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="df950-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-136">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-138">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="df950-139">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="df950-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-141">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-143">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="df950-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="df950-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df950-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df950-145">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="df950-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="df950-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df950-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-148">Indique si le port réseau peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="df950-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="df950-149">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-150">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="df950-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-153">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="df950-153">The primary availability and status of the device.</span></span> <span data-ttu-id="df950-154">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="df950-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-156">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-158">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="df950-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="df950-159">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="df950-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="df950-160">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="df950-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="df950-161">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="df950-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="df950-162">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="df950-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-164">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-166">Fonctionnalités du port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="df950-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="df950-167">Si les fonctionnalités de basculement ou d’équilibrage de charge sont répertoriées, un [**\_ SpareGroup CIM**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (basculement) ou un [**\_ ExtraCapacityGroup CIM**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (équilibrage de charge) doit également être défini pour décrire complètement la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="df950-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="df950-168">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="df950-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="df950-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df950-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="df950-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df950-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="df950-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="df950-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wakeonlan** (3)</span><span class="sxs-lookup"><span data-stu-id="df950-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="df950-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Basculement** (4)</span><span class="sxs-lookup"><span data-stu-id="df950-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="df950-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="df950-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df950-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="df950-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-176">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df950-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-178">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités de port Ethernet indiquées dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="df950-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="df950-179">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="df950-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="df950-180">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-181">**Caption**</span><span class="sxs-lookup"><span data-stu-id="df950-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-184">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="df950-184">A short description of the object.</span></span> <span data-ttu-id="df950-185">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df950-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-186">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="df950-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-189">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="df950-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="df950-190">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="df950-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df950-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df950-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-195">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="df950-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="df950-196">Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="df950-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="df950-197">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df950-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df950-198">**Description**</span><span class="sxs-lookup"><span data-stu-id="df950-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-201">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="df950-201">A description of the object.</span></span> <span data-ttu-id="df950-202">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df950-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="df950-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-204">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-206">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="df950-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="df950-207">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="df950-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df950-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="df950-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-212">Une adresse ou d’autres informations d’identification utilisées pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="df950-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="df950-213">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="df950-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="df950-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="df950-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-216">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="df950-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="df950-217">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="df950-217">A display name for the object.</span></span> <span data-ttu-id="df950-218">Cette propriété permet à chaque instance de définir un nom complet en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="df950-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="df950-219">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et est générée en fonction de la carte réseau présente dans l’hôte.</span><span class="sxs-lookup"><span data-stu-id="df950-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="df950-220">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df950-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-221">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-223">Spécifie les fonctionnalités qui sont activées dans la liste de tous les types pris en charge, qui sont définis dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="df950-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="df950-224">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="df950-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="df950-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df950-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="df950-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df950-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="df950-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="df950-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wakeonlan** (3)</span><span class="sxs-lookup"><span data-stu-id="df950-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="df950-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Basculement** (4)</span><span class="sxs-lookup"><span data-stu-id="df950-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="df950-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="df950-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df950-231">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="df950-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-232">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-234">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="df950-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="df950-235">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df950-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="df950-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-239">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="df950-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="df950-240">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df950-241">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="df950-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-242">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="df950-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df950-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-244">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="df950-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="df950-245">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="df950-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-249">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="df950-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="df950-250">Cette propriété est héritée de la propriété [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-251">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="df950-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-252">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="df950-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df950-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-254">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="df950-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="df950-255">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="df950-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-259">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="df950-259">The current health of the element.</span></span> <span data-ttu-id="df950-260">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="df950-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="df950-261">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="df950-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-263">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df950-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-265">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="df950-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="df950-266">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés **OtherIdentifyingInfo** situé dans le même index.</span><span class="sxs-lookup"><span data-stu-id="df950-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="df950-267">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="df950-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-269">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="df950-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df950-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-271">Valeur **DateTime** qui indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="df950-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="df950-272">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="df950-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="df950-273">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="df950-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df950-277">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="df950-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="df950-278">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="df950-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="df950-279">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df950-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="df950-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-281">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df950-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df950-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-283">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="df950-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="df950-284">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-285">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="df950-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-286">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-288">Types de liens.</span><span class="sxs-lookup"><span data-stu-id="df950-288">The types of links.</span></span> <span data-ttu-id="df950-289">Si la valeur 1 (autre) est définie, la propriété associée **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="df950-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="df950-290">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="df950-291">Valeur</span><span class="sxs-lookup"><span data-stu-id="df950-291">Value</span></span>                                                                        | <span data-ttu-id="df950-292">Signification</span><span class="sxs-lookup"><span data-stu-id="df950-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="df950-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="df950-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="df950-294">Ethernet</span><span class="sxs-lookup"><span data-stu-id="df950-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="df950-295">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="df950-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-296">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df950-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df950-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-298">Taille maximale du champ INFO (non-MAC) qui sera reçu ou transmis.</span><span class="sxs-lookup"><span data-stu-id="df950-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="df950-299">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-300">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="df950-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-301">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-303">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="df950-303">This property has been deprecated.</span></span> <span data-ttu-id="df950-304">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-305">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="df950-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-306">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-307">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-308">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="df950-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="df950-309">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df950-310">**Nom**</span><span class="sxs-lookup"><span data-stu-id="df950-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-313">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="df950-313">The label by which the object is known.</span></span> <span data-ttu-id="df950-314">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="df950-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="df950-315">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="df950-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-317">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df950-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-319">Les adresses MAC Ethernet/802.3 au format 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques (le bit d’adresse de groupe se trouve dans le bit de poids faible du premier caractère de la chaîne). Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="df950-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-321">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-323">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="df950-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="df950-324">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="df950-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df950-325">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="df950-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-327">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-329">États actuels de l’élément.</span><span class="sxs-lookup"><span data-stu-id="df950-329">The current statuses of the element.</span></span> <span data-ttu-id="df950-330">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-331">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df950-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-332">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df950-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-334">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités activées spécifiées comme 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="df950-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="df950-335">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="df950-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-339">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre). Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="df950-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="df950-340">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df950-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="df950-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-342">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df950-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-344">Toutes les données, en plus des informations d’ID de l’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="df950-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="df950-345">Par exemple, vous pouvez utiliser cette propriété pour stocker le nom complet du système d’exploitation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="df950-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="df950-346">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-347">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="df950-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-350">Valeur de chaîne qui décrit la propriété **LinkTechnology** lorsqu’elle a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="df950-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="df950-351">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-352">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="df950-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-355">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="df950-355">This property is deprecated.</span></span> <span data-ttu-id="df950-356">Utilisez la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="df950-356">Use the **PortType** property.</span></span> <span data-ttu-id="df950-357">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="df950-358">Description déconseillée : type de module, lorsque la propriété **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="df950-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="df950-359">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="df950-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-362">Type de module, lorsque la propriété **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="df950-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="df950-363">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="df950-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="df950-364">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="df950-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-367">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="df950-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="df950-368">Cette adresse peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="df950-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="df950-369">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="df950-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="df950-370">Elle doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="df950-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="df950-371">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-372">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="df950-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-373">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-375">Les ports réseau sont souvent numérotés par rapport à un module logique ou à un élément réseau.</span><span class="sxs-lookup"><span data-stu-id="df950-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="df950-376">Cette valeur est 1 pour les cartes réseau émulées, 0 pour toutes les autres.</span><span class="sxs-lookup"><span data-stu-id="df950-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="df950-377">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="df950-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-379">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-381">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="df950-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="df950-382">Si la valeur 1 (autre) est définie, la propriété associée **OtherPortType** contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="df950-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="df950-383">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="df950-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="df950-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="df950-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df950-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="df950-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df950-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 cuivre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="df950-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="df950-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="df950-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="df950-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="df950-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="df950-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="df950-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="df950-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="df950-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="df950-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="df950-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="df950-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="df950-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="df950-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="df950-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="df950-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="df950-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="df950-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="df950-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="df950-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="df950-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="df950-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="df950-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="df950-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="df950-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="df950-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="df950-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="df950-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="df950-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="df950-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="df950-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="df950-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="df950-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="df950-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="df950-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="df950-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-SEM** (111)</span><span class="sxs-lookup"><span data-stu-id="df950-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="df950-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="df950-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df950-406">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df950-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-407">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-409">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="df950-409">The power management capabilities of the device.</span></span> <span data-ttu-id="df950-410">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="df950-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-412">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="df950-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df950-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-414">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="df950-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="df950-415">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-416">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="df950-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-417">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-419">Nombre d’heures consécutives pendant lesquelles ce périphérique a été alimenté depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="df950-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="df950-420">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-421">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="df950-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-422">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-424">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="df950-424">Provides high level status information.</span></span> <span data-ttu-id="df950-425">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="df950-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="df950-426">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="df950-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df950-427">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="df950-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-429">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-431">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="df950-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="df950-432">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="df950-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="df950-433">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df950-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="df950-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-435">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-437">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="df950-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="df950-438">Lorsque la propriété **EnabledState** a la valeur 5 (non applicable), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="df950-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="df950-439">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df950-440">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="df950-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-441">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df950-443">Qualificateurs : **override**, **Units** ("bits par seconde")</span><span class="sxs-lookup"><span data-stu-id="df950-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="df950-444">Bande passante actuelle du port en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="df950-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="df950-445">Pour les ports qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.</span><span class="sxs-lookup"><span data-stu-id="df950-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="df950-446">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-447">**État**</span><span class="sxs-lookup"><span data-stu-id="df950-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-450">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="df950-450">The current status of the object.</span></span> <span data-ttu-id="df950-451">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-452">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="df950-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-453">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="df950-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df950-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-455">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="df950-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="df950-456">Les entrées de ce tableau sont corrélées avec celles situées au même index de tableau dans **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="df950-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="df950-457">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df950-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df950-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="df950-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-459">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-461">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="df950-461">The state of the logical device.</span></span> <span data-ttu-id="df950-462">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-463">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="df950-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-464">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df950-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df950-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-466">Unité de transmission maximale (MTU) qui peut être prise en charge.</span><span class="sxs-lookup"><span data-stu-id="df950-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="df950-467">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df950-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df950-468">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df950-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-471">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="df950-471">The scoping system's creation class name.</span></span> <span data-ttu-id="df950-472">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas prise en charge</span><span class="sxs-lookup"><span data-stu-id="df950-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="df950-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="df950-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="df950-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df950-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-476">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="df950-476">The name of the scoping system.</span></span> <span data-ttu-id="df950-477">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df950-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df950-478">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="df950-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-479">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="df950-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df950-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-481">Date ou heure de la dernière modification de la propriété **EnabledState** de l’élément.</span><span class="sxs-lookup"><span data-stu-id="df950-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="df950-482">Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="df950-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="df950-483">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="df950-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="df950-484">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="df950-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-486">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-488">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="df950-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="df950-489">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="df950-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-491">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-493">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="df950-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="df950-494">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df950-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df950-495">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="df950-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df950-496">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df950-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df950-497">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="df950-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df950-498">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="df950-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="df950-499">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df950-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="df950-500">Valeur</span><span class="sxs-lookup"><span data-stu-id="df950-500">Value</span></span>                                                                        | <span data-ttu-id="df950-501">Signification</span><span class="sxs-lookup"><span data-stu-id="df950-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="df950-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="df950-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="df950-503">Non restreint</span><span class="sxs-lookup"><span data-stu-id="df950-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df950-504">Notes</span><span class="sxs-lookup"><span data-stu-id="df950-504">Remarks</span></span>

<span data-ttu-id="df950-505">L’accès à la classe **MSVM \_ InternalEthernetPort** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="df950-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="df950-506">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="df950-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="df950-507">Exemples</span><span class="sxs-lookup"><span data-stu-id="df950-507">Examples</span></span>

<span data-ttu-id="df950-508">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="df950-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df950-509">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df950-509">Requirements</span></span>



| <span data-ttu-id="df950-510">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df950-510">Requirement</span></span> | <span data-ttu-id="df950-511">Valeur</span><span class="sxs-lookup"><span data-stu-id="df950-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df950-512">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df950-512">Minimum supported client</span></span><br/> | <span data-ttu-id="df950-513">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df950-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="df950-514">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df950-514">Minimum supported server</span></span><br/> | <span data-ttu-id="df950-515">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df950-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df950-516">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="df950-516">Namespace</span></span><br/>                | <span data-ttu-id="df950-517">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="df950-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="df950-518">MOF</span><span class="sxs-lookup"><span data-stu-id="df950-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df950-519"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df950-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df950-520">DLL</span><span class="sxs-lookup"><span data-stu-id="df950-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df950-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df950-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df950-522">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df950-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df950-523">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="df950-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="df950-524">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="df950-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

