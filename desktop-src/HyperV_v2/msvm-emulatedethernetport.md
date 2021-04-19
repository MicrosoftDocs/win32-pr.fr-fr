---
description: Représente un adaptateur Ethernet émulé.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Msvm_EmulatedEthernetPort, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520458"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="95fa7-103">MSVM \_ EmulatedEthernetPort, classe</span><span class="sxs-lookup"><span data-stu-id="95fa7-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="95fa7-104">Représente un adaptateur Ethernet émulé.</span><span class="sxs-lookup"><span data-stu-id="95fa7-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="95fa7-105">Cet adaptateur est utilisé lorsqu’un ordinateur virtuel ne peut pas exécuter le port Ethernet synthétique quand aucun circuit intégré n’est installé dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="95fa7-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="95fa7-106">Cette classe n’est pas disponible pour les ordinateurs virtuels de génération 2.</span><span class="sxs-lookup"><span data-stu-id="95fa7-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="95fa7-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="95fa7-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fa7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95fa7-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
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
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="95fa7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="95fa7-109">Members</span></span>

<span data-ttu-id="95fa7-110">La classe **MSVM \_ EmulatedEthernetPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="95fa7-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="95fa7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95fa7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="95fa7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="95fa7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95fa7-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="95fa7-113">Methods</span></span>

<span data-ttu-id="95fa7-114">La classe **MSVM \_ EmulatedEthernetPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="95fa7-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="95fa7-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="95fa7-115">Method</span></span>                                                                     | <span data-ttu-id="95fa7-116">Description</span><span class="sxs-lookup"><span data-stu-id="95fa7-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="95fa7-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="95fa7-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="95fa7-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="95fa7-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="95fa7-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="95fa7-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="95fa7-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="95fa7-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="95fa7-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="95fa7-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="95fa7-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="95fa7-124">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="95fa7-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="95fa7-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="95fa7-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="95fa7-126">Réinitialise l’appareil émulé.</span><span class="sxs-lookup"><span data-stu-id="95fa7-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="95fa7-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="95fa7-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="95fa7-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="95fa7-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="95fa7-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="95fa7-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="95fa7-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="95fa7-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="95fa7-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="95fa7-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="95fa7-133">Properties</span></span>

<span data-ttu-id="95fa7-134">La classe **MSVM \_ EmulatedEthernetPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="95fa7-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95fa7-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="95fa7-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-136">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95fa7-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-138">Unité de transmission maximale (MTU) active ou négociée qui peut être prise en charge.</span><span class="sxs-lookup"><span data-stu-id="95fa7-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="95fa7-139">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur 1500.</span><span class="sxs-lookup"><span data-stu-id="95fa7-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="95fa7-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-141">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-143">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="95fa7-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (« non applicable »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-145">**Détection automatique**</span><span class="sxs-lookup"><span data-stu-id="95fa7-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="95fa7-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-148">Indique si le port réseau peut déterminer automatiquement la vitesse ou d’autres caractéristiques de communication du support réseau attaché.</span><span class="sxs-lookup"><span data-stu-id="95fa7-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="95fa7-149">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="95fa7-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-150">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="95fa7-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-153">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95fa7-153">The primary availability and status of the device.</span></span> <span data-ttu-id="95fa7-154">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="95fa7-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="95fa7-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-156">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-158">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="95fa7-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="95fa7-159">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="95fa7-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="95fa7-160">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="95fa7-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="95fa7-161">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="95fa7-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="95fa7-162">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="95fa7-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="95fa7-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="95fa7-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="95fa7-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="95fa7-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="95fa7-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="95fa7-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="95fa7-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="95fa7-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="95fa7-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="95fa7-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="95fa7-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="95fa7-173">)</span><span class="sxs-lookup"><span data-stu-id="95fa7-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="95fa7-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="95fa7-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-175">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-177">Fonctionnalités du port Ethernet.</span><span class="sxs-lookup"><span data-stu-id="95fa7-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="95fa7-178">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-179">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="95fa7-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-180">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95fa7-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-182">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités de port Ethernet indiquées dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="95fa7-183">Notez que chaque entrée de ce tableau est liée à l’entrée dans le tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="95fa7-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="95fa7-184">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-185">**Caption**</span><span class="sxs-lookup"><span data-stu-id="95fa7-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-188">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="95fa7-188">A short description of the object.</span></span> <span data-ttu-id="95fa7-189">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-190">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="95fa7-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-193">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="95fa7-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="95fa7-194">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="95fa7-195">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="95fa7-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95fa7-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-199">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="95fa7-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="95fa7-200">Quand elle est utilisée avec les autres propriétés de clé de cette classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="95fa7-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="95fa7-201">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ EmulatedEthernetPort ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-202">**Description**</span><span class="sxs-lookup"><span data-stu-id="95fa7-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-205">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="95fa7-205">A description of the object.</span></span> <span data-ttu-id="95fa7-206">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « port Ethernet émulé Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="95fa7-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-210">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="95fa7-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="95fa7-211">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="95fa7-212">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="95fa7-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="95fa7-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-216">Une adresse ou d’autres informations d’identification utilisées pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95fa7-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="95fa7-217">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID* \\ *Device-Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="95fa7-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="95fa7-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-221">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="95fa7-221">A display name for the object.</span></span> <span data-ttu-id="95fa7-222">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « carte réseau héritée ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-223">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="95fa7-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-224">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-226">Les fonctionnalités qui sont activées dans la liste de tous les éléments pris en charge, qui sont définis dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="95fa7-227">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-228">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="95fa7-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-229">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-231">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="95fa7-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="95fa7-232">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et est toujours définie sur 2 (« activé »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="95fa7-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-234">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-236">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="95fa7-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="95fa7-237">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 5 (« non applicable »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="95fa7-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-239">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="95fa7-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-241">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="95fa7-242">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="95fa7-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-246">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="95fa7-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="95fa7-247">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-248">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="95fa7-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-249">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="95fa7-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-251">Indique si le port fonctionne en mode duplex intégral.</span><span class="sxs-lookup"><span data-stu-id="95fa7-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="95fa7-252">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="95fa7-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="95fa7-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-254">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-256">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="95fa7-256">The current health of the element.</span></span> <span data-ttu-id="95fa7-257">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="95fa7-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="95fa7-258">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (« OK »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="95fa7-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-260">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95fa7-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-262">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="95fa7-263">Chaque entrée de ce tableau est liée à l’entrée dans **OtherIdentifyingInfo** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="95fa7-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="95fa7-264">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="95fa7-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-266">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95fa7-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-268">Valeur **DateTime** qui indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="95fa7-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="95fa7-269">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="95fa7-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="95fa7-270">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="95fa7-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="95fa7-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-274">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="95fa7-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-275">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="95fa7-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="95fa7-276">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="95fa7-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="95fa7-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-278">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95fa7-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-280">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95fa7-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="95fa7-281">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-282">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="95fa7-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-285">Types de liens.</span><span class="sxs-lookup"><span data-stu-id="95fa7-285">The types of links.</span></span> <span data-ttu-id="95fa7-286">Si la valeur 1 (« other ») est définie, la propriété associée **OtherLinkTechnology** contient une description de chaîne du type de lien.</span><span class="sxs-lookup"><span data-stu-id="95fa7-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="95fa7-287">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) et a toujours la valeur 2 (« Ethernet »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-288">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="95fa7-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-289">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95fa7-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-291">Taille maximale du champ INFO (non-MAC) qui sera reçu ou transmis.</span><span class="sxs-lookup"><span data-stu-id="95fa7-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="95fa7-292">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et est toujours définie sur 1500.</span><span class="sxs-lookup"><span data-stu-id="95fa7-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-293">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="95fa7-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-294">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95fa7-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-297">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="95fa7-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-298">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95fa7-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-300">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="95fa7-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="95fa7-301">Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))et est toujours définie sur 1 milliard.</span><span class="sxs-lookup"><span data-stu-id="95fa7-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-302">**Nom**</span><span class="sxs-lookup"><span data-stu-id="95fa7-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-305">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="95fa7-305">The label by which the object is known.</span></span> <span data-ttu-id="95fa7-306">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="95fa7-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="95fa7-307">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « port Ethernet ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-308">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="95fa7-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-309">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95fa7-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-311">Les adresses MAC Ethernet/802.3, au format 12 chiffres hexadécimaux (par exemple, « 010203040506 »), chaque paire représentant l’un des six octets de l’adresse MAC dans l’ordre des bits canoniques (le bit d’adresse de groupe se trouve dans le bit de poids faible du premier caractère de la chaîne).</span><span class="sxs-lookup"><span data-stu-id="95fa7-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="95fa7-312">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-313">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="95fa7-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-314">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-316">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="95fa7-317">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="95fa7-318">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="95fa7-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="95fa7-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-320">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-322">États actuels de l’élément.</span><span class="sxs-lookup"><span data-stu-id="95fa7-322">The current statuses of the element.</span></span> <span data-ttu-id="95fa7-323">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 2 (« OK »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-324">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="95fa7-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-325">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95fa7-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-327">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités activées spécifiées comme « other ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="95fa7-328">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="95fa7-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-332">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="95fa7-333">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="95fa7-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="95fa7-334">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="95fa7-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-336">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95fa7-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-338">Toutes les données, en plus des informations d’ID de l’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="95fa7-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="95fa7-339">Par exemple, vous pouvez utiliser cette propriété pour stocker le nom complet du système d’exploitation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95fa7-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="95fa7-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="95fa7-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-344">Valeur de chaîne qui décrit **LinkTechnology** lorsqu’il a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="95fa7-345">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="95fa7-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-349">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="95fa7-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-350">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="95fa7-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-351">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-353">Type de module, lorsque **portType** a la valeur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="95fa7-354">Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) et est toujours définie sur « Ethernet virtuel ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-355">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="95fa7-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-358">Adresse réseau qui est codée en dur dans un port.</span><span class="sxs-lookup"><span data-stu-id="95fa7-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="95fa7-359">Cette adresse peut être modifiée à l’aide d’une mise à niveau du microprogramme ou d’une configuration logicielle.</span><span class="sxs-lookup"><span data-stu-id="95fa7-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="95fa7-360">Lorsque cette modification est apportée, le champ doit être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="95fa7-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="95fa7-361">Elle doit être laissée vide si aucune adresse codée en dur n’existe pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="95fa7-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="95fa7-362">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="95fa7-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-363">**Numéroport**</span><span class="sxs-lookup"><span data-stu-id="95fa7-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-364">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-366">Les ports réseau sont souvent numérotés par rapport à un module logique ou à un élément réseau.</span><span class="sxs-lookup"><span data-stu-id="95fa7-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="95fa7-367">Cette propriété est héritée de la [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="95fa7-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="95fa7-368">Valeur</span><span class="sxs-lookup"><span data-stu-id="95fa7-368">Value</span></span>                                                                        | <span data-ttu-id="95fa7-369">Signification</span><span class="sxs-lookup"><span data-stu-id="95fa7-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="95fa7-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="95fa7-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="95fa7-371">La carte d’interface réseau n’est pas émulée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="95fa7-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="95fa7-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="95fa7-373">La carte d’interface réseau est émulée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="95fa7-374">**PortType**</span><span class="sxs-lookup"><span data-stu-id="95fa7-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-375">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-377">Mode spécifique actuellement activé pour le port.</span><span class="sxs-lookup"><span data-stu-id="95fa7-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="95fa7-378">Si la valeur 1 (« other ») est définie, la propriété associée **OtherPortType** contient une description de chaîne du type de port.</span><span class="sxs-lookup"><span data-stu-id="95fa7-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="95fa7-379">Cette propriété est héritée de [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)et est toujours définie sur 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-380">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="95fa7-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-381">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-383">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="95fa7-383">The power management capabilities of the device.</span></span> <span data-ttu-id="95fa7-384">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="95fa7-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-386">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="95fa7-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-388">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="95fa7-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="95fa7-389">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-390">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="95fa7-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-391">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95fa7-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-393">Nombre d’heures consécutives pendant lesquelles ce périphérique a été alimenté depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="95fa7-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="95fa7-394">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-395">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="95fa7-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-396">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-398">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="95fa7-398">Provides high level status information.</span></span> <span data-ttu-id="95fa7-399">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="95fa7-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="95fa7-400">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="95fa7-401">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="95fa7-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-402">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="95fa7-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-403">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95fa7-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-405">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="95fa7-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="95fa7-406">La bande passante réelle est indiquée dans LogicalPort. Speed.</span><span class="sxs-lookup"><span data-stu-id="95fa7-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="95fa7-407">Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))et est toujours définie sur 1 milliard.</span><span class="sxs-lookup"><span data-stu-id="95fa7-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="95fa7-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-409">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-411">Dernier État demandé ou souhaité pour le service de gestion.</span><span class="sxs-lookup"><span data-stu-id="95fa7-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="95fa7-412">Quand **EnabledState** a la valeur 5 (« non applicable »), cette propriété n’a aucune signification.</span><span class="sxs-lookup"><span data-stu-id="95fa7-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="95fa7-413">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (« non applicable »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-414">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="95fa7-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-415">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95fa7-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-417">Bande passante actuelle du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="95fa7-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="95fa7-418">Pour les ports qui varient en bande passante ou pour ceux pour lesquels aucune estimation précise ne peut être effectuée, cette propriété doit contenir la bande passante nominale.</span><span class="sxs-lookup"><span data-stu-id="95fa7-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="95fa7-419">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur 1 milliard.</span><span class="sxs-lookup"><span data-stu-id="95fa7-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-420">**État**</span><span class="sxs-lookup"><span data-stu-id="95fa7-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-423">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-424">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="95fa7-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-425">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="95fa7-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-427">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="95fa7-428">Les entrées de ce tableau sont corrélées avec celles situées au même index de tableau dans **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="95fa7-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="95fa7-429">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="95fa7-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-431">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-433">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="95fa7-433">The state of the logical device.</span></span> <span data-ttu-id="95fa7-434">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-435">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="95fa7-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-438">Qualificateurs : **Units** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="95fa7-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-439">Unité de transmission maximale (MTU) qui peut être prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="95fa7-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="95fa7-440">Cette propriété est héritée de [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)et est toujours définie sur 1500.</span><span class="sxs-lookup"><span data-stu-id="95fa7-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-441">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95fa7-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-444">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="95fa7-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="95fa7-445">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="95fa7-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-446">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="95fa7-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-447">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fa7-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-448">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-449">ID de machine virtuelle sous forme de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="95fa7-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="95fa7-450">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="95fa7-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-451">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="95fa7-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-452">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95fa7-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-454">Date ou heure de la dernière modification de l' **EnabledState** de l’élément.</span><span class="sxs-lookup"><span data-stu-id="95fa7-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="95fa7-455">Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="95fa7-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="95fa7-456">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="95fa7-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="95fa7-457">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-458">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="95fa7-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-459">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-461">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="95fa7-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="95fa7-462">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-463">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="95fa7-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-464">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-466">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="95fa7-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="95fa7-467">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="95fa7-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="95fa7-468">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="95fa7-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95fa7-469">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95fa7-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95fa7-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="95fa7-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95fa7-471">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="95fa7-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="95fa7-472">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (« non restreint »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="95fa7-473">Cette propriété est héritée de [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) et a toujours la valeur 4 (« non restreint »).</span><span class="sxs-lookup"><span data-stu-id="95fa7-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95fa7-474">Notes</span><span class="sxs-lookup"><span data-stu-id="95fa7-474">Remarks</span></span>

<span data-ttu-id="95fa7-475">L’accès à la classe **MSVM \_ EmulatedEthernetPort** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="95fa7-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="95fa7-476">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="95fa7-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="95fa7-477">Exemples</span><span class="sxs-lookup"><span data-stu-id="95fa7-477">Examples</span></span>

<span data-ttu-id="95fa7-478">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="95fa7-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95fa7-479">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95fa7-479">Requirements</span></span>



| <span data-ttu-id="95fa7-480">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95fa7-480">Requirement</span></span> | <span data-ttu-id="95fa7-481">Valeur</span><span class="sxs-lookup"><span data-stu-id="95fa7-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95fa7-482">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95fa7-482">Minimum supported client</span></span><br/> | <span data-ttu-id="95fa7-483">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95fa7-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95fa7-484">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95fa7-484">Minimum supported server</span></span><br/> | <span data-ttu-id="95fa7-485">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95fa7-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95fa7-486">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="95fa7-486">Namespace</span></span><br/>                | <span data-ttu-id="95fa7-487">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="95fa7-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="95fa7-488">MOF</span><span class="sxs-lookup"><span data-stu-id="95fa7-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95fa7-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95fa7-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95fa7-490">DLL</span><span class="sxs-lookup"><span data-stu-id="95fa7-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95fa7-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95fa7-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95fa7-492">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95fa7-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fa7-493">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="95fa7-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="95fa7-494">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="95fa7-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

