---
description: Représente un système d’ordinateur physique ou un ordinateur virtuel.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551878"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="0e802-103">\_Classe MSVM ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="0e802-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="0e802-104">Représente un système d’ordinateur physique ou un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="0e802-105">Pour récupérer des informations pour le VMMS, utilisez la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0e802-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="0e802-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e802-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e802-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e802-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="0e802-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0e802-108">Members</span></span>

<span data-ttu-id="0e802-109">La classe **MSVM \_ ComputerSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e802-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="0e802-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e802-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e802-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e802-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e802-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0e802-112">Methods</span></span>

<span data-ttu-id="0e802-113">La classe **MSVM \_ ComputerSystem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0e802-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="0e802-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="0e802-114">Method</span></span>                                                                                         | <span data-ttu-id="0e802-115">Description</span><span class="sxs-lookup"><span data-stu-id="0e802-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e802-116">**InjectNonMaskableInterrupt**</span><span class="sxs-lookup"><span data-stu-id="0e802-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="0e802-117">Injecte une interruption non masquable dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="0e802-118">Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="0e802-119">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="0e802-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="0e802-120">**RequestReplicationStateChange**</span><span class="sxs-lookup"><span data-stu-id="0e802-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="0e802-121">Demande que l’état de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0e802-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="0e802-122">Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="0e802-123">**RequestReplicationStateChangeEx**</span><span class="sxs-lookup"><span data-stu-id="0e802-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="0e802-124">Demande que l’état de réplication de l’ordinateur virtuel soit remplacé par la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0e802-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="0e802-125">Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="0e802-126">**Windows 8.1 :** Cette méthode n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="0e802-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="0e802-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0e802-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="0e802-128">Demande que l’état de l’ordinateur virtuel soit modifié.</span><span class="sxs-lookup"><span data-stu-id="0e802-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="0e802-129">Cette méthode est prise en charge uniquement pour les instances de la classe **MSVM \_ ComputerSystem** qui représentent un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="0e802-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0e802-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="0e802-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e802-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="0e802-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e802-132">Properties</span></span>

<span data-ttu-id="0e802-133">La classe **MSVM \_ ComputerSystem** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0e802-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e802-134">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0e802-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-135">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-137">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="0e802-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0e802-138">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0e802-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="0e802-139">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0e802-140">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0e802-141">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e802-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0e802-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="0e802-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="0e802-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="0e802-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="0e802-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="0e802-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="0e802-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="0e802-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="0e802-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0e802-152">)</span><span class="sxs-lookup"><span data-stu-id="0e802-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e802-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0e802-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-154">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-156">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e802-156">A short description of the object.</span></span> <span data-ttu-id="0e802-157">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="0e802-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-158">Value</span></span>                                                                                                | <span data-ttu-id="0e802-159">Signification</span><span class="sxs-lookup"><span data-stu-id="0e802-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0e802-160"><dt>« Ordinateur virtuel »</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="0e802-161">L’instance représente une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="0e802-162"><dt>« Système informatique d’hébergement »</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="0e802-163">L’instance représente l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="0e802-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e802-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0e802-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-165">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-167">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0e802-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0e802-168">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0e802-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e802-169">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-170">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0e802-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-173">Nom de la classe ou de la sous-classe utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="0e802-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="0e802-174">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="0e802-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0e802-175">**Dédié**</span><span class="sxs-lookup"><span data-stu-id="0e802-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-176">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-178">Indique si le système informatique est un système à usage spécifique (dédié à une utilisation particulière) et s’il s’agit d’un système à usage général.</span><span class="sxs-lookup"><span data-stu-id="0e802-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="0e802-179">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 0 (non dédié).</span><span class="sxs-lookup"><span data-stu-id="0e802-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-180">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e802-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-183">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="0e802-183">A description of the object.</span></span> <span data-ttu-id="0e802-184">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="0e802-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-185">Value</span></span>                                                                                                          | <span data-ttu-id="0e802-186">Signification</span><span class="sxs-lookup"><span data-stu-id="0e802-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0e802-187"><dt>« Système d’ordinateur virtuel Microsoft »</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="0e802-188">L’instance représente une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="0e802-189"><dt>« Système informatique d’hébergement Microsoft »</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="0e802-190">L’instance représente l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="0e802-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e802-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0e802-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-192">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-194">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0e802-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0e802-195">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0e802-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e802-196">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0e802-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-200">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e802-200">A display name for the object.</span></span> <span data-ttu-id="0e802-201">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur le nom d’affichage de l’ordinateur pour un ordinateur virtuel ou le nom NetBIOS du système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="0e802-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0e802-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-203">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-205">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="0e802-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0e802-206">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0e802-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e802-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Activé mais hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="0e802-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e802-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0e802-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-213">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="0e802-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0e802-214">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="0e802-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0e802-215">Cette propriété est héritée de la classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et est définie sur 2 (activé) pour un ordinateur physique ou sur l’une des valeurs suivantes pour une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="0e802-216">Pour obtenir une vue graphique de ces États, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0e802-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="0e802-217">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="0e802-218">Signification</span><span class="sxs-lookup"><span data-stu-id="0e802-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="0e802-219"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="0e802-220">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0e802-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="0e802-221"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="0e802-222"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="0e802-223">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0e802-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="0e802-224"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="0e802-225">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0e802-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="0e802-226"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="0e802-227">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="0e802-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="0e802-228"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="0e802-229">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="0e802-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="0e802-230"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="0e802-231">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="0e802-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="0e802-232"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="0e802-233">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="0e802-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="0e802-234"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="0e802-235">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="0e802-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="0e802-236"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="0e802-237">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="0e802-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="0e802-238">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="0e802-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="0e802-239">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0e802-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="0e802-240">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="0e802-241">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="0e802-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="0e802-242">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="0e802-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="0e802-243">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="0e802-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-246">Spécifie l’état actuel du mode de session étendu sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="0e802-247">Le fournisseur WMI Hyper-V déclenche un [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) chaque fois que le **EnhancedSessionModeState** de la classe **MSVM \_ ComputerSystem** change.</span><span class="sxs-lookup"><span data-stu-id="0e802-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="0e802-248">Si une session vmconnection active reçoit un **\_ \_ InstanceModificationEvent**, elle tente de basculer en mode de session étendu si l’utilisateur a activé ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0e802-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="0e802-249">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="0e802-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="0e802-250">**EnhancedSessionModeState** peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e802-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="0e802-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Autorisé et disponible** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e802-252">Le mode étendu est autorisé et disponible sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="0e802-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non autorisé** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e802-254">Le mode étendu n’est pas autorisé sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="0e802-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Autorisé mais non disponible** (6)</span><span class="sxs-lookup"><span data-stu-id="0e802-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0e802-256">Le mode étendu est autorisé et n’est pas disponible actuellement sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e802-257">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="0e802-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-258">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-260">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="0e802-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-261">Type de point de données de récupération appliqué pendant l’opération de basculement.</span><span class="sxs-lookup"><span data-stu-id="0e802-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-262">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="0e802-263">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e802-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0e802-264">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="0e802-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="0e802-265">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="0e802-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="0e802-266">**Cohérence des applications** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="0e802-267">**Planifiée** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e802-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0e802-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-269">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-271">Spécifie l’intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0e802-271">Specifies the current health of the element.</span></span> <span data-ttu-id="0e802-272">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="0e802-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="0e802-273">Lorsqu’une erreur critique se produit, consultez le journal des événements pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0e802-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="0e802-274">La propriété **EnabledState** peut également contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0e802-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="0e802-275">Par exemple, lorsque l’espace disque est très faible, **HealthState** est défini sur 25, l’ordinateur virtuel s’interrompt et **EnabledState** a la valeur 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="0e802-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="0e802-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="0e802-277">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="0e802-278">Signification</span><span class="sxs-lookup"><span data-stu-id="0e802-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="0e802-279"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="0e802-280">L’ordinateur virtuel est entièrement fonctionnel et fonctionne dans des paramètres opérationnels normaux et sans erreur.</span><span class="sxs-lookup"><span data-stu-id="0e802-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="0e802-281"><dt>**Erreur majeure**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="0e802-282">L’ordinateur virtuel a subi un échec majeur.</span><span class="sxs-lookup"><span data-stu-id="0e802-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="0e802-283">Cette valeur est utilisée lorsqu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque et que l’ordinateur virtuel a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="0e802-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="0e802-284"><dt>**Erreur critique**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="0e802-285">L’élément n’est pas fonctionnel et la récupération n’est peut-être pas possible.</span><span class="sxs-lookup"><span data-stu-id="0e802-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="0e802-286">Cela peut indiquer que le processus de travail de l’ordinateur virtuel (Vmwp.exe) ne répond pas aux demandes de contrôle ou d’informations, ou qu’un ou plusieurs disques contenant les disques durs virtuels de l’ordinateur virtuel manquent d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="0e802-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e802-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e802-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-288">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e802-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-290">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e802-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-292">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-294">Date et heure de création de la configuration d’ordinateur virtuel pour un ordinateur virtuel, ou **valeur null**, pour un système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="0e802-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="0e802-295">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0e802-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-299">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="0e802-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0e802-300">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0e802-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0e802-301">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="0e802-302">Dans Windows 8, il existe une seule instance de [**ReplicationSettingData**](msvm-replicationsettingdata.md) pour chaque système informatique ou ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="0e802-303">Par Windows 8.1, une machine virtuelle de récupération a deux instances de **ReplicationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="0e802-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="0e802-304">Ce changement différencie et associe les données de paramètres à la relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="0e802-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="0e802-305">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="0e802-305">Property name</span></span>  | <span data-ttu-id="0e802-306">Valeur Windows 8</span><span class="sxs-lookup"><span data-stu-id="0e802-306">Windows 8 value</span></span>               | <span data-ttu-id="0e802-307">Valeur Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0e802-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="0e802-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0e802-308">**InstanceID**</span></span> | <span data-ttu-id="0e802-309">Microsoft : <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="0e802-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="0e802-310">Microsoft : <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="0e802-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="0e802-311">Dans la valeur Windows 8.1, 0 indique primaire et 1 indique la réplication étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="0e802-312">Pour plus d’informations sur la réplication étendue, consultez [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="0e802-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-313">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-314">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-316">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="0e802-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-317">Heure à laquelle la dernière réplication de cohérence des applications a été reçue pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-318">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="0e802-319">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-320">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-322">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="0e802-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-323">Heure à laquelle la dernière réplication est reçue lors de la récupération de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-324">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="0e802-325">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="0e802-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-326">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-328">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="0e802-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-329">Type de la dernière réplication qui a été reçue pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-330">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="0e802-331">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e802-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0e802-332">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="0e802-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="0e802-333">**Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="0e802-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="0e802-334">**Cohérence des applications** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="0e802-335">**Planifiée** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e802-336">**LastSuccessfulBackupTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-337">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-339">Heure à laquelle la dernière sauvegarde réussie est terminée pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-340">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0e802-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-343">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0e802-343">The label by which the object is known.</span></span> <span data-ttu-id="0e802-344">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur «*GUID*».</span><span class="sxs-lookup"><span data-stu-id="0e802-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="0e802-345">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="0e802-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-348">Chaîne qui identifie la façon dont le nom système a été généré, à l’aide de la méthode heuristique de sous-classe.</span><span class="sxs-lookup"><span data-stu-id="0e802-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="0e802-349">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-350">**Nœuds NUMA**</span><span class="sxs-lookup"><span data-stu-id="0e802-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-351">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-353">Nombre de nœuds NUMA (ununiform Memory Access) du système informatique.</span><span class="sxs-lookup"><span data-stu-id="0e802-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="0e802-354">Quand **MSVM \_ ComputerSystem** représente le système informatique d’hébergement, cette propriété contient le nombre de nœuds NUMA physiques.</span><span class="sxs-lookup"><span data-stu-id="0e802-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="0e802-355">Quand **MSVM \_ ComputerSystem** représente un ordinateur virtuel, cette propriété contient le nombre de nœuds NUMA virtuels qui sont présentés au système d’exploitation invité par le biais de la table d’affinité des ressources système (SRAT) ACPI.</span><span class="sxs-lookup"><span data-stu-id="0e802-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-356">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="0e802-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-357">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0e802-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-359">Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« millisecondes »)</span><span class="sxs-lookup"><span data-stu-id="0e802-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-360">Pour la machine virtuelle, cette propriété indique la durée, en millisecondes, depuis la dernière activation, réinitialisation ou restauration de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e802-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="0e802-361">Cette fois, vous excluez l’heure à laquelle la machine virtuelle était à l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="0e802-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="0e802-362">Pour le système d’exploitation de gestion, cette propriété a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0e802-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-364">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-366">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0e802-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0e802-367">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0e802-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e802-368">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0e802-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-370">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-372">Tableau qui contient les États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0e802-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="0e802-373">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="0e802-374">La valeur à l’index zéro (0) est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="0e802-375">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="0e802-376">Signification</span><span class="sxs-lookup"><span data-stu-id="0e802-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="0e802-377"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="0e802-378">L’ordinateur virtuel est fonctionnel et fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="0e802-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="0e802-379"><dt>**Dégradé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="0e802-380">L’ordinateur virtuel ne fonctionne que partiellement.</span><span class="sxs-lookup"><span data-stu-id="0e802-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="0e802-381">Cela indique que le stockage qui contient la configuration n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="0e802-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="0e802-382">Une machine virtuelle dans cet État peut uniquement être désactivée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="0e802-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="0e802-383"><dt>**Échec prédictif**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="0e802-384">L’ordinateur virtuel est fonctionnel mais peut échouer à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="0e802-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="0e802-385">Cela indique que l’espace libre est insuffisant sur le stockage qui contient le disque dur virtuel de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="0e802-386">L’ordinateur virtuel sera mis en pause si l’espace disque disponible est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="0e802-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="0e802-387"><dt></dt> <dt>10</dt> arrêtés</span><span class="sxs-lookup"><span data-stu-id="0e802-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="0e802-388">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e802-388">This value is not supported.</span></span> <span data-ttu-id="0e802-389">Si la machine virtuelle est arrêtée, la propriété **EnabledState** aura la valeur 3 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="0e802-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="0e802-390"><dt>**Dans le service**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="0e802-391">L’ordinateur virtuel est en cours de traitement d’une demande.</span><span class="sxs-lookup"><span data-stu-id="0e802-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="0e802-392"><dt>**Dormant**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="0e802-393">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e802-393">This value is not supported.</span></span> <span data-ttu-id="0e802-394">Si la machine virtuelle est interrompue ou suspendue, la propriété **EnabledState** aura la valeur 32769 (suspendu) ou 32768 (suspendu).</span><span class="sxs-lookup"><span data-stu-id="0e802-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="0e802-395">La valeur à l’index 1 (1) est facultative et contient des informations d’état secondaire.</span><span class="sxs-lookup"><span data-stu-id="0e802-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="0e802-396">Un client doit utiliser l’état principal de l’index zéro (0) pour déterminer si une nouvelle demande peut être émise pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="0e802-397">Si **OperationalStatus** \[ 0 \] est égal à 2 (OK), l’opération indiquée par **OperationalStatus** \[ 1 \] peut être interrompue.</span><span class="sxs-lookup"><span data-stu-id="0e802-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="0e802-398">La valeur à **OperationalStatus** \[ 1 \] est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="0e802-399">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0e802-400">Signification</span><span class="sxs-lookup"><span data-stu-id="0e802-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="0e802-401"><dt>**Création de l’instantané**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="0e802-402">Un instantané est en cours de création pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="0e802-403"><dt>**Application de l’instantané**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="0e802-404">Un instantané est en cours d’application sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="0e802-405"><dt>**Suppression de l’instantané**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="0e802-406">Un instantané est en cours de suppression de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="0e802-407"><dt>**En attente de démarrage de**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="0e802-408">L’ordinateur virtuel démarre une fois que le délai de démarrage automatique s’est écoulé.</span><span class="sxs-lookup"><span data-stu-id="0e802-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="0e802-409"><dt>**Fusion des disques**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="0e802-410">Les disques durs virtuels des instantanés précédemment supprimés sont en cours de fusion.</span><span class="sxs-lookup"><span data-stu-id="0e802-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="0e802-411"><dt>**Exportation de l’ordinateur virtuel**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="0e802-412">L’ordinateur virtuel est en cours d’exportation.</span><span class="sxs-lookup"><span data-stu-id="0e802-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="0e802-413"><dt>**Migration de la machine virtuelle**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="0e802-414">L’ordinateur virtuel est en cours de migration dynamique d’un ordinateur physique vers un autre.</span><span class="sxs-lookup"><span data-stu-id="0e802-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="0e802-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e802-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-416">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e802-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-418">Chaîne qui décrit comment ou pourquoi le système est dédié lorsque le tableau **dédié** comprend la valeur 2 (autre).</span><span class="sxs-lookup"><span data-stu-id="0e802-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="0e802-419">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-420">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0e802-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-423">État activé ou désactivé de l’ordinateur virtuel lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="0e802-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0e802-424">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="0e802-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0e802-425">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0e802-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-427">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e802-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-429">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0e802-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-431">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-433">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e802-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-434">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="0e802-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-435">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-437">Chaîne qui indique comment le propriétaire du système principal peut être atteint (par exemple, un numéro de téléphone ou une adresse de messagerie).</span><span class="sxs-lookup"><span data-stu-id="0e802-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="0e802-438">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-439">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="0e802-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-440">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-442">Nom du propriétaire du système principal.</span><span class="sxs-lookup"><span data-stu-id="0e802-442">The name of the primary system owner.</span></span> <span data-ttu-id="0e802-443">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-444">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0e802-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-445">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-447">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="0e802-447">Provides high level status information.</span></span> <span data-ttu-id="0e802-448">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="0e802-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0e802-449">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0e802-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0e802-450">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="0e802-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-452">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e802-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-454">Identificateur du processus sous lequel cet ordinateur virtuel est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0e802-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="0e802-455">Cette valeur peut être utilisée pour identifier de façon unique l’instance de Vmwp.exe sur le système qui exécute l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-456">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="0e802-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-457">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-459">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span><span class="sxs-lookup"><span data-stu-id="0e802-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-460">Intégrité de la réplication pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-461">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="0e802-462">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e802-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0e802-463">**Non applicable** (0)</span><span class="sxs-lookup"><span data-stu-id="0e802-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="0e802-464">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0e802-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0e802-465">**Avertissement** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="0e802-466">**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e802-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="0e802-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-468">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-470">Spécifie le mode de réplication pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="0e802-471">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="0e802-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="0e802-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="0e802-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (1)</span><span class="sxs-lookup"><span data-stu-id="0e802-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="0e802-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e802-475">Récupération</span><span class="sxs-lookup"><span data-stu-id="0e802-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="0e802-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Réplica de test** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0e802-477">Réplica</span><span class="sxs-lookup"><span data-stu-id="0e802-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="0e802-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Réplica étendu** (4)</span><span class="sxs-lookup"><span data-stu-id="0e802-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e802-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="0e802-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-480">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-482">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span><span class="sxs-lookup"><span data-stu-id="0e802-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-483">État de réplication de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e802-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="0e802-484">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt la propriété du même nom dans la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour obtenir la valeur de la relation principale ou étendue.</span><span class="sxs-lookup"><span data-stu-id="0e802-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="0e802-485">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0e802-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e802-486">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="0e802-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="0e802-487">**Prêt pour la réplication** (1)</span><span class="sxs-lookup"><span data-stu-id="0e802-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="0e802-488">**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="0e802-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="0e802-489">**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="0e802-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="0e802-490">**Réplication synchronisée terminée** (4)</span><span class="sxs-lookup"><span data-stu-id="0e802-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="0e802-491">**Récupéré** (5)</span><span class="sxs-lookup"><span data-stu-id="0e802-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="0e802-492">**Validé** (6)</span><span class="sxs-lookup"><span data-stu-id="0e802-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="0e802-493">**Suspendu** (7)</span><span class="sxs-lookup"><span data-stu-id="0e802-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="0e802-494">**Critique** (8)</span><span class="sxs-lookup"><span data-stu-id="0e802-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="0e802-495">**En attente de démarrage de la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="0e802-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="0e802-496">**Resynchronisation** (10)</span><span class="sxs-lookup"><span data-stu-id="0e802-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="0e802-497">**Resynchronisation suspendue** (11)</span><span class="sxs-lookup"><span data-stu-id="0e802-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="0e802-498">**Basculement en cours** (12)</span><span class="sxs-lookup"><span data-stu-id="0e802-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="0e802-499">**Restauration automatique en cours** (13)</span><span class="sxs-lookup"><span data-stu-id="0e802-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="0e802-500">**Restauration automatique terminée** (14)</span><span class="sxs-lookup"><span data-stu-id="0e802-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e802-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0e802-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-502">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-503">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-504">Dernier État demandé ou souhaité pour l’ordinateur virtuel passé à la méthode [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , ou 12 (non applicable) si aucun changement d’État n’est en cours.</span><span class="sxs-lookup"><span data-stu-id="0e802-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="0e802-505">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="0e802-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0e802-506">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="0e802-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0e802-507">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e802-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-508">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="0e802-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-509">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-510">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-511">Cette propriété est héritée de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)et est toujours définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="0e802-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-512">**Rôles**</span><span class="sxs-lookup"><span data-stu-id="0e802-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-513">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e802-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-515">Tableau de chaînes qui décrivent les rôles joués par le système dans l’environnement informatique.</span><span class="sxs-lookup"><span data-stu-id="0e802-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="0e802-516">Cette propriété est héritée [**du \_ système CIM**](/windows/desktop/CIMWin32Prov/cim-system)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0e802-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-517">**État**</span><span class="sxs-lookup"><span data-stu-id="0e802-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-518">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e802-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-520">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e802-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-521">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e802-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-522">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0e802-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e802-523">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e802-524">Qualificateurs : **arrayType** ("indexé")</span><span class="sxs-lookup"><span data-stu-id="0e802-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0e802-525">Tableau qui contient des chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="0e802-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="0e802-526">Par exemple, si 11 (en service) est la valeur affectée à **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] peut contenir une explication sur la raison pour laquelle l’ordinateur virtuel traite une demande.</span><span class="sxs-lookup"><span data-stu-id="0e802-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="0e802-527">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0e802-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-528">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="0e802-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-529">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-531">Date et heure de la dernière modification du fichier de configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="0e802-532">Le fichier de configuration est modifié lors de certaines opérations d’ordinateur virtuel, ainsi que lors de l’ajout, de la modification ou de la suppression de l’un des paramètres de l’ordinateur virtuel ou de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0e802-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-533">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0e802-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-534">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e802-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-535">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-536">Date et heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0e802-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0e802-537">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0e802-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-538">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0e802-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e802-539">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0e802-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e802-540">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0e802-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e802-541">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="0e802-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0e802-542">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0e802-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e802-543">Notes</span><span class="sxs-lookup"><span data-stu-id="0e802-543">Remarks</span></span>

<span data-ttu-id="0e802-544">L’illustration suivante montre les valeurs **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0e802-544">The following illustration shows the **EnabledState** values.</span></span>

![diagramme d’État pour les valeurs enabledState pour Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="0e802-546">Quand une propriété de la classe **MSVM \_ ComputerSystem** change, le fournisseur WMI indique un événement [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) qui décrit les modifications.</span><span class="sxs-lookup"><span data-stu-id="0e802-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="0e802-547">L’état précédent est contenu dans la propriété **PreviousInstance** , et le nouvel État est contenu dans la propriété **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="0e802-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="0e802-548">Cet événement est asynchrone ; au moment du traitement de l’événement **\_ \_ InstanceModificationEvent** , la propriété **TargetInstance** peut ne pas refléter l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="0e802-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="0e802-549">L’accès à la classe **MSVM \_ ComputerSystem** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="0e802-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0e802-550">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0e802-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0e802-551">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e802-551">Examples</span></span>

<span data-ttu-id="0e802-552">Consultez [interrogation d’objets de mise en réseau](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0e802-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e802-553">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e802-553">Requirements</span></span>



| <span data-ttu-id="0e802-554">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e802-554">Requirement</span></span> | <span data-ttu-id="0e802-555">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e802-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e802-556">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e802-556">Minimum supported client</span></span><br/> | <span data-ttu-id="0e802-557">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e802-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0e802-558">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e802-558">Minimum supported server</span></span><br/> | <span data-ttu-id="0e802-559">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e802-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e802-560">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e802-560">Namespace</span></span><br/>                | <span data-ttu-id="0e802-561">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e802-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0e802-562">MOF</span><span class="sxs-lookup"><span data-stu-id="0e802-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e802-563"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e802-564">DLL</span><span class="sxs-lookup"><span data-stu-id="0e802-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e802-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e802-566">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e802-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e802-567">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="0e802-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="0e802-568">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="0e802-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="0e802-569">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="0e802-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="0e802-570">**MSVM \_ ComputerSystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="0e802-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="0e802-571">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="0e802-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

