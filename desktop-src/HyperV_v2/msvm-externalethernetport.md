---
description: Représente un port Ethernet externe (carte réseau).
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Msvm_ExternalEthernetPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526853"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="8b443-103">MSVM \_ ExternalEthernetPort, classe</span><span class="sxs-lookup"><span data-stu-id="8b443-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="8b443-104">Représente un port Ethernet externe (carte réseau).</span><span class="sxs-lookup"><span data-stu-id="8b443-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="8b443-105">Ces types de ports Ethernet permettent aux machines virtuelles d’accéder au réseau externe.</span><span class="sxs-lookup"><span data-stu-id="8b443-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="8b443-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8b443-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b443-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b443-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="8b443-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8b443-108">Members</span></span>

<span data-ttu-id="8b443-109">La classe **MSVM \_ ExternalEthernetPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b443-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="8b443-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b443-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b443-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b443-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b443-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b443-112">Methods</span></span>

<span data-ttu-id="8b443-113">La classe **MSVM \_ ExternalEthernetPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8b443-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="8b443-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="8b443-114">Method</span></span>                                                                     | <span data-ttu-id="8b443-115">Description</span><span class="sxs-lookup"><span data-stu-id="8b443-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="8b443-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="8b443-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="8b443-117">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b443-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b443-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="8b443-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="8b443-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b443-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b443-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="8b443-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="8b443-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b443-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="8b443-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8b443-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="8b443-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="8b443-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="8b443-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="8b443-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="8b443-125">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="8b443-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="8b443-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="8b443-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="8b443-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b443-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b443-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="8b443-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="8b443-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b443-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b443-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8b443-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="8b443-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b443-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8b443-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b443-132">Properties</span></span>

<span data-ttu-id="8b443-133">La classe **MSVM \_ ExternalEthernetPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8b443-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b443-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="8b443-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-137">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8b443-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8b443-138">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="8b443-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="8b443-139">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="8b443-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-141">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-143">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="8b443-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="8b443-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-145">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="8b443-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8b443-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-148">Indique si le port réseau peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="8b443-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="8b443-149">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-150">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="8b443-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-153">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8b443-153">The primary availability and status of the device.</span></span> <span data-ttu-id="8b443-154">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8b443-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-156">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-158">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="8b443-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="8b443-159">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="8b443-160">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="8b443-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="8b443-161">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="8b443-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="8b443-162">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="8b443-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="8b443-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="8b443-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="8b443-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="8b443-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="8b443-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="8b443-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="8b443-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="8b443-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="8b443-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="8b443-173">)</span><span class="sxs-lookup"><span data-stu-id="8b443-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b443-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8b443-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-175">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-177">Tableau qui spécifie les fonctionnalités du port.</span><span class="sxs-lookup"><span data-stu-id="8b443-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="8b443-178">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8b443-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b443-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8b443-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="8b443-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wakeonlan** (3)</span><span class="sxs-lookup"><span data-stu-id="8b443-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Basculement** (4)</span><span class="sxs-lookup"><span data-stu-id="8b443-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="8b443-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b443-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8b443-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-186">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-188">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités de port contenues dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="8b443-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="8b443-189">Chaque entrée de ce tableau est liée à l’entrée correspondante dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="8b443-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="8b443-190">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8b443-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8b443-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-194">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="8b443-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8b443-195">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8b443-195">A short description of the object.</span></span> <span data-ttu-id="8b443-196">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="8b443-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8b443-197">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8b443-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-200">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="8b443-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8b443-201">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8b443-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b443-202">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-203">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b443-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-206">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8b443-206">The scoping system's creation class name.</span></span> <span data-ttu-id="8b443-207">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ ExternalEthernetPort ».</span><span class="sxs-lookup"><span data-stu-id="8b443-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="8b443-208">**Description**</span><span class="sxs-lookup"><span data-stu-id="8b443-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-211">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="8b443-211">A description of the object.</span></span> <span data-ttu-id="8b443-212">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet externe Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="8b443-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="8b443-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8b443-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-214">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-216">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8b443-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8b443-217">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8b443-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b443-218">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-219">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8b443-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-222">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8b443-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="8b443-223">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b443-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8b443-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-227">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8b443-227">A display name for the object.</span></span> <span data-ttu-id="8b443-228">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-229">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8b443-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-230">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-232">Spécifie les fonctionnalités qui sont activées dans la liste de toutes les fonctionnalités prises en charge dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="8b443-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="8b443-233">Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8b443-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b443-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8b443-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="8b443-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**Wakeonlan** (3)</span><span class="sxs-lookup"><span data-stu-id="8b443-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Basculement** (4)</span><span class="sxs-lookup"><span data-stu-id="8b443-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="8b443-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b443-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8b443-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-241">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-243">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8b443-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="8b443-244">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="8b443-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8b443-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-246">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-248">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="8b443-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8b443-249">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="8b443-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8b443-250">Par exemple, l’arrêt (4) et le démarrage de (10) sont des États transitoires entre activé et désactivé.</span><span class="sxs-lookup"><span data-stu-id="8b443-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="8b443-251">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8b443-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b443-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8b443-253">Signification</span><span class="sxs-lookup"><span data-stu-id="8b443-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="8b443-254"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="8b443-255"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="8b443-256"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="8b443-257">L’élément est ou peut exécuter des commandes, traite toutes les commandes mises en file d’attente et met en file d’attente les nouvelles requêtes.</span><span class="sxs-lookup"><span data-stu-id="8b443-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="8b443-258"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="8b443-259">L’élément n’exécutera pas de commande et supprimera toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="8b443-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="8b443-260"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="8b443-261">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="8b443-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="8b443-262"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="8b443-263">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="8b443-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="8b443-264"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="8b443-265">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="8b443-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="8b443-266"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="8b443-267">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="8b443-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="8b443-268"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="8b443-269">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="8b443-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="8b443-270"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="8b443-271">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="8b443-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="8b443-272">Le comportement de l’élément est similaire à l’état activé, mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="8b443-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="8b443-273">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8b443-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="8b443-274">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="8b443-275">L’élément est en train d’accéder à un état activé.</span><span class="sxs-lookup"><span data-stu-id="8b443-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="8b443-276">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="8b443-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="8b443-277"><dt>**DMTF réservé**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="8b443-278">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8b443-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="8b443-279"><dt>**Fournisseur réservé**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="8b443-280">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8b443-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="8b443-281">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8b443-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-282">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8b443-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-284">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="8b443-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="8b443-285">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8b443-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-287">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-289">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="8b443-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="8b443-290">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-291">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="8b443-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-292">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8b443-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-294">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="8b443-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="8b443-295">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8b443-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-297">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-299">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8b443-299">The current health of the element.</span></span> <span data-ttu-id="8b443-300">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="8b443-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8b443-301">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="8b443-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8b443-302">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="8b443-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8b443-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-304">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-306">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="8b443-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="8b443-307">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8b443-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-309">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b443-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-311">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8b443-311">The date and time when the object was installed.</span></span> <span data-ttu-id="8b443-312">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="8b443-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="8b443-313">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8b443-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-315">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-317">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="8b443-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8b443-318">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="8b443-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8b443-319">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-320">**IsBound**</span><span class="sxs-lookup"><span data-stu-id="8b443-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-321">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8b443-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-323">Si cette propriété a la **valeur true**, ce port Ethernet peut être connecté aux commutateurs et peut donc fournir une connectivité à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8b443-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="8b443-324">Si cette propriété a la **valeur false**, ce port Ethernet n’est pas utilisé par l’architecture réseau de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8b443-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-325">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8b443-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-326">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b443-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-328">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8b443-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="8b443-329">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-330">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="8b443-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-331">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-333">Spécifie le type de technologie de lien pour le port.</span><span class="sxs-lookup"><span data-stu-id="8b443-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="8b443-334">Lorsque la valeur 1 (autre) est définie, la propriété **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="8b443-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="8b443-335">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b443-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8b443-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="8b443-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="8b443-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="8b443-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="8b443-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="8b443-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span><span class="sxs-lookup"><span data-stu-id="8b443-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Relais de trames** (8)</span><span class="sxs-lookup"><span data-stu-id="8b443-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarouge** (9)</span><span class="sxs-lookup"><span data-stu-id="8b443-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="8b443-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Réseau local sans fil** (11)</span><span class="sxs-lookup"><span data-stu-id="8b443-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b443-348">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="8b443-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-349">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b443-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-351">Taille maximale du champ INFO (non-MAC) qui sera reçu ou transmis.</span><span class="sxs-lookup"><span data-stu-id="8b443-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="8b443-352">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et est toujours définie sur 1500.</span><span class="sxs-lookup"><span data-stu-id="8b443-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-353">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="8b443-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-354">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-356">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="8b443-356">This property has been deprecated.</span></span> <span data-ttu-id="8b443-357">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-358">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="8b443-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-359">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-361">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="8b443-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="8b443-362">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="8b443-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="8b443-363">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-364">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8b443-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-367">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="8b443-367">The label by which the object is known.</span></span> <span data-ttu-id="8b443-368">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-369">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="8b443-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-370">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-372">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="8b443-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="8b443-373">Tableau de chaînes qui contient les adresses MAC du port.</span><span class="sxs-lookup"><span data-stu-id="8b443-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="8b443-374">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-375">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8b443-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-378">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8b443-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8b443-379">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8b443-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b443-380">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8b443-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-382">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-384">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8b443-384">The current statuses of the object.</span></span> <span data-ttu-id="8b443-385">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="8b443-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-386">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8b443-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-387">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-389">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités activées spécifiées comme 1 (autre). Cette propriété est héritée de la [**\_ EthernetPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="8b443-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-390">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8b443-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-393">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="8b443-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8b443-394">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="8b443-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8b443-395">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8b443-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-397">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-399">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="8b443-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="8b443-400">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-401">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="8b443-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-402">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-404">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="8b443-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="8b443-405">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-406">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="8b443-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-407">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-409">L’utilisation de cette propriété est déconseillée à la place de la propriété **portType** .</span><span class="sxs-lookup"><span data-stu-id="8b443-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="8b443-410">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-411">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="8b443-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-414">Type de module, lorsque **portType** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="8b443-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="8b443-415">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-416">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="8b443-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-417">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-419">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="8b443-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8b443-420">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="8b443-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="8b443-421">Cette adresse codée en dur peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="8b443-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="8b443-422">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="8b443-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="8b443-423">Cette propriété doit avoir la **valeur null** s’il n’existe aucune adresse codée en dur pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="8b443-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="8b443-424">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-425">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="8b443-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-426">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-427">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-428">Le numéro de port.</span><span class="sxs-lookup"><span data-stu-id="8b443-428">The port number.</span></span> <span data-ttu-id="8b443-429">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-430">**PortType**</span><span class="sxs-lookup"><span data-stu-id="8b443-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-431">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-433">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="8b443-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="8b443-434">Si la valeur 1 (« other ») est définie, la propriété associée **OtherPortType** contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="8b443-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="8b443-435">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b443-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="8b443-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 cuivre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="8b443-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="8b443-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="8b443-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="8b443-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="8b443-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="8b443-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="8b443-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 fibre 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="8b443-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="8b443-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="8b443-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="8b443-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="8b443-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="8b443-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="8b443-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="8b443-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="8b443-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="8b443-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="8b443-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-SEM** (111)</span><span class="sxs-lookup"><span data-stu-id="8b443-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="8b443-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b443-458">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8b443-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-459">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-461">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="8b443-461">The power management capabilities of the device.</span></span> <span data-ttu-id="8b443-462">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-463">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8b443-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-464">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8b443-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-466">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8b443-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="8b443-467">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-468">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8b443-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-469">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-471">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="8b443-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="8b443-472">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-473">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8b443-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-474">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-476">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="8b443-476">Provides high level status information.</span></span> <span data-ttu-id="8b443-477">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="8b443-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="8b443-478">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="8b443-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b443-479">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-480">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="8b443-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-481">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-482">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-483">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="8b443-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="8b443-484">Bande passante demandée du port en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="8b443-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="8b443-485">La bande passante réelle est indiquée dans la propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="8b443-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="8b443-486">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8b443-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-488">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-489">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-490">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="8b443-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="8b443-491">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="8b443-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-492">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="8b443-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-493">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-494">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-495">Qualificateurs : **unités** (« bits par seconde »)</span><span class="sxs-lookup"><span data-stu-id="8b443-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="8b443-496">La bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="8b443-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="8b443-497">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-498">**État**</span><span class="sxs-lookup"><span data-stu-id="8b443-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-501">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8b443-501">The current status of the object.</span></span> <span data-ttu-id="8b443-502">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b443-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-503">OK</span><span class="sxs-lookup"><span data-stu-id="8b443-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="8b443-504"><span id="OK"></span><span id="ok"></span>**Bien**</span><span class="sxs-lookup"><span data-stu-id="8b443-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreurs**</span><span class="sxs-lookup"><span data-stu-id="8b443-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré**</span><span class="sxs-lookup"><span data-stu-id="8b443-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Connue**</span><span class="sxs-lookup"><span data-stu-id="8b443-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Échec prévu**</span><span class="sxs-lookup"><span data-stu-id="8b443-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarr**</span><span class="sxs-lookup"><span data-stu-id="8b443-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt**</span><span class="sxs-lookup"><span data-stu-id="8b443-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Services**</span><span class="sxs-lookup"><span data-stu-id="8b443-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Trop sollicité**</span><span class="sxs-lookup"><span data-stu-id="8b443-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Non récupéré**</span><span class="sxs-lookup"><span data-stu-id="8b443-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact**</span><span class="sxs-lookup"><span data-stu-id="8b443-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Communication perdue**</span><span class="sxs-lookup"><span data-stu-id="8b443-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b443-516">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8b443-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-517">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="8b443-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b443-518">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-519">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8b443-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8b443-520">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="8b443-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="8b443-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8b443-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-522">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-523">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-524">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="8b443-524">The current state of the logical device.</span></span> <span data-ttu-id="8b443-525">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-526">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="8b443-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-527">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-528">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b443-529">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="8b443-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8b443-530">Unité de transmission maximale (MTU) qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="8b443-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="8b443-531">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="8b443-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b443-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-533">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-534">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-535">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8b443-535">The scoping system's creation class name.</span></span> <span data-ttu-id="8b443-536">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="8b443-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="8b443-537">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8b443-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-538">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8b443-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-539">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-540">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="8b443-540">The name of the scoping system.</span></span> <span data-ttu-id="8b443-541">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b443-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b443-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8b443-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-543">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b443-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-544">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-545">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="8b443-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8b443-546">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="8b443-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-547">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8b443-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-548">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b443-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-549">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-550">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="8b443-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="8b443-551">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-552">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8b443-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-553">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-554">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-555">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="8b443-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8b443-556">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8b443-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b443-557">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="8b443-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b443-558">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b443-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b443-559">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b443-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b443-560">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="8b443-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="8b443-561">C’est le cas, par exemple, d’un groupe de stockage qui peut avoir back end ports pour communiquer avec les lecteurs de disque et les ports frontaux pour communiquer avec les hôtes.</span><span class="sxs-lookup"><span data-stu-id="8b443-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="8b443-562">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur « non restreint ».</span><span class="sxs-lookup"><span data-stu-id="8b443-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="8b443-563">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b443-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8b443-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="8b443-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Frontal uniquement** (2)</span><span class="sxs-lookup"><span data-stu-id="8b443-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Serveur principal uniquement** (3)</span><span class="sxs-lookup"><span data-stu-id="8b443-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b443-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Non restreint** (4)</span><span class="sxs-lookup"><span data-stu-id="8b443-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b443-568">Notes</span><span class="sxs-lookup"><span data-stu-id="8b443-568">Remarks</span></span>

<span data-ttu-id="8b443-569">L’accès à la classe **MSVM \_ ExternalEthernetPort** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="8b443-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8b443-570">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8b443-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8b443-571">Exemples</span><span class="sxs-lookup"><span data-stu-id="8b443-571">Examples</span></span>

<span data-ttu-id="8b443-572">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8b443-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b443-573">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b443-573">Requirements</span></span>



| <span data-ttu-id="8b443-574">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b443-574">Requirement</span></span> | <span data-ttu-id="8b443-575">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b443-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b443-576">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b443-576">Minimum supported client</span></span><br/> | <span data-ttu-id="8b443-577">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b443-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b443-578">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b443-578">Minimum supported server</span></span><br/> | <span data-ttu-id="8b443-579">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b443-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b443-580">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b443-580">Namespace</span></span><br/>                | <span data-ttu-id="8b443-581">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8b443-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b443-582">MOF</span><span class="sxs-lookup"><span data-stu-id="8b443-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b443-583"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b443-584">DLL</span><span class="sxs-lookup"><span data-stu-id="8b443-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b443-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b443-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b443-586">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b443-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b443-587">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="8b443-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="8b443-588">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="8b443-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

