---
description: Représente l’état du service de pulsation, qui est responsable de la surveillance de l’état d’un ordinateur virtuel en signalant une pulsation à intervalles réguliers.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Classe Msvm_HeartbeatComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525228"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="0201e-103">MSVM \_ HeartbeatComponent, classe</span><span class="sxs-lookup"><span data-stu-id="0201e-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="0201e-104">Représente l’état du service de pulsation, qui est responsable de la surveillance de l’état d’un ordinateur virtuel en signalant une pulsation à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="0201e-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="0201e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0201e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0201e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0201e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
};
```

## <a name="members"></a><span data-ttu-id="0201e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0201e-107">Members</span></span>

<span data-ttu-id="0201e-108">La classe **MSVM \_ HeartbeatComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0201e-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="0201e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0201e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0201e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0201e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0201e-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0201e-111">Methods</span></span>

<span data-ttu-id="0201e-112">La classe **MSVM \_ HeartbeatComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0201e-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="0201e-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="0201e-113">Method</span></span>                                                                   | <span data-ttu-id="0201e-114">Description</span><span class="sxs-lookup"><span data-stu-id="0201e-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="0201e-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="0201e-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="0201e-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0201e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0201e-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="0201e-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="0201e-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0201e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0201e-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="0201e-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="0201e-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0201e-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="0201e-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0201e-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="0201e-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="0201e-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="0201e-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="0201e-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="0201e-124">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="0201e-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="0201e-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="0201e-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="0201e-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0201e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0201e-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="0201e-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="0201e-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0201e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="0201e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0201e-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="0201e-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0201e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0201e-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0201e-131">Properties</span></span>

<span data-ttu-id="0201e-132">La classe **MSVM \_ HeartbeatComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0201e-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0201e-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="0201e-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-136">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0201e-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="0201e-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="0201e-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="0201e-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-141">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0201e-141">The primary availability and status of the device.</span></span> <span data-ttu-id="0201e-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="0201e-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-144">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-146">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="0201e-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="0201e-147">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel du [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0201e-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="0201e-148">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="0201e-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="0201e-149">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="0201e-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="0201e-150">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0201e-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0201e-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="0201e-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="0201e-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="0201e-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="0201e-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="0201e-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="0201e-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="0201e-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="0201e-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="0201e-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0201e-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF réservé** (..</span><span class="sxs-lookup"><span data-stu-id="0201e-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0201e-161">)</span><span class="sxs-lookup"><span data-stu-id="0201e-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0201e-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0201e-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-165">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0201e-165">A short description of the object.</span></span> <span data-ttu-id="0201e-166">Cette propriété est héritée de la classe [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) et est toujours définie sur « pulsation ».</span><span class="sxs-lookup"><span data-stu-id="0201e-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="0201e-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0201e-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-170">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="0201e-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0201e-171">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0201e-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0201e-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-173">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0201e-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-176">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0201e-176">The scoping system's creation class name.</span></span> <span data-ttu-id="0201e-177">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ HeartbeatComponent ».</span><span class="sxs-lookup"><span data-stu-id="0201e-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="0201e-178">**Description**</span><span class="sxs-lookup"><span data-stu-id="0201e-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-181">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="0201e-181">A description of the object.</span></span> <span data-ttu-id="0201e-182">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de pulsation Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="0201e-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="0201e-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0201e-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-186">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0201e-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0201e-187">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0201e-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0201e-188">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-189">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0201e-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-192">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0201e-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="0201e-193">Cette propriété est héritée [**de CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*VMGUID* \\ *GUID*», où *VMGUID* est la propriété **Name** de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associée à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0201e-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0201e-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-197">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0201e-197">A display name for the object.</span></span> <span data-ttu-id="0201e-198">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « pulsation ».</span><span class="sxs-lookup"><span data-stu-id="0201e-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="0201e-199">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="0201e-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-200">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-202">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 7 (pas de valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="0201e-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0201e-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-204">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-206">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="0201e-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0201e-207">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0201e-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="0201e-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="0201e-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="0201e-209">Signification</span><span class="sxs-lookup"><span data-stu-id="0201e-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="0201e-210"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0201e-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="0201e-211">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0201e-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="0201e-212"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0201e-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0201e-213">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="0201e-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0201e-214">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="0201e-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-215">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0201e-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-217">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="0201e-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="0201e-218">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0201e-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-222">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="0201e-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="0201e-223">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0201e-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-225">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-227">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0201e-227">The current health of the element.</span></span> <span data-ttu-id="0201e-228">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="0201e-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0201e-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-230">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0201e-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-232">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="0201e-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="0201e-233">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0201e-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-235">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0201e-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-237">Date et heure auxquelles le service d’intégration a été installé sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0201e-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="0201e-238">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0201e-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0201e-242">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="0201e-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0201e-243">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0201e-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0201e-244">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-245">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="0201e-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-246">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0201e-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-248">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0201e-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="0201e-249">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-250">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="0201e-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-251">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0201e-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-253">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="0201e-253">This property has been deprecated.</span></span> <span data-ttu-id="0201e-254">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-255">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0201e-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-258">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="0201e-258">The label by which the object is known.</span></span> <span data-ttu-id="0201e-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-260">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0201e-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-261">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-263">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0201e-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0201e-264">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0201e-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0201e-265">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0201e-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-267">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0201e-269">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span><span class="sxs-lookup"><span data-stu-id="0201e-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0201e-270">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0201e-270">The current status of the element.</span></span> <span data-ttu-id="0201e-271">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="0201e-272">Les valeurs possibles pour la valeur de la propriété **OperationalStatus** 0 sont les suivantes \[ \] .</span><span class="sxs-lookup"><span data-stu-id="0201e-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0201e-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0201e-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-274">Le service fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="0201e-274">The service is operating normally.</span></span> <span data-ttu-id="0201e-275">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0201e-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0201e-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (3)</span><span class="sxs-lookup"><span data-stu-id="0201e-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-277">Le service fonctionne normalement, mais le service invité a négocié une version de protocole de communication compatible.</span><span class="sxs-lookup"><span data-stu-id="0201e-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="0201e-278">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0201e-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0201e-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="0201e-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-280">L’invité ne prend pas en charge une version de protocole compatible.</span><span class="sxs-lookup"><span data-stu-id="0201e-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="0201e-281">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0201e-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0201e-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (12)</span><span class="sxs-lookup"><span data-stu-id="0201e-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-283">Le service invité n’est pas installé ou n’a pas encore été contacté.</span><span class="sxs-lookup"><span data-stu-id="0201e-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0201e-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Perte de communication** (13)</span><span class="sxs-lookup"><span data-stu-id="0201e-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-285">Le service invité ne répond plus normalement.</span><span class="sxs-lookup"><span data-stu-id="0201e-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0201e-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (15)</span><span class="sxs-lookup"><span data-stu-id="0201e-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-287">L’ordinateur virtuel est en pause.</span><span class="sxs-lookup"><span data-stu-id="0201e-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="0201e-288">La valeur de la propriété **OperationalStatus** \[ 1 \] indique les valeurs de l’état de l’application fusionnée.</span><span class="sxs-lookup"><span data-stu-id="0201e-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="0201e-289">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0201e-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="0201e-290">L’état d’une application est défini sur l’ordinateur virtuel à l’aide de la méthode [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) .</span><span class="sxs-lookup"><span data-stu-id="0201e-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0201e-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0201e-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-292">Les applications qui s’exécutent à l’intérieur de la machine virtuelle fonctionnent normalement.</span><span class="sxs-lookup"><span data-stu-id="0201e-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="0201e-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Incompatibilité de protocole** (32775)</span><span class="sxs-lookup"><span data-stu-id="0201e-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-294">L’invité et les composants hôtes exécutent des versions de protocole différentes.</span><span class="sxs-lookup"><span data-stu-id="0201e-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="0201e-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**État critique** de l’Application (32782)</span><span class="sxs-lookup"><span data-stu-id="0201e-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-296">Une ou plusieurs applications à l’intérieur de la machine virtuelle sont dans un état critique.</span><span class="sxs-lookup"><span data-stu-id="0201e-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="0201e-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>Expiration du **délai de communication** (32783)</span><span class="sxs-lookup"><span data-stu-id="0201e-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-298">Expiration du délai d’attente d’une réponse du composant invité.</span><span class="sxs-lookup"><span data-stu-id="0201e-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="0201e-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Échec** de la Communication (32784)</span><span class="sxs-lookup"><span data-stu-id="0201e-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="0201e-300">Échec de la communication avec le composant invité.</span><span class="sxs-lookup"><span data-stu-id="0201e-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0201e-301">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0201e-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-304">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="0201e-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0201e-305">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="0201e-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="0201e-306">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0201e-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="0201e-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-308">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0201e-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-310">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="0201e-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="0201e-311">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et prend toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="0201e-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-312">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0201e-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-313">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-315">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0201e-315">The power management capabilities of the device.</span></span> <span data-ttu-id="0201e-316">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-317">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="0201e-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-318">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0201e-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-320">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="0201e-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="0201e-321">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-322">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0201e-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-323">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0201e-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-325">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="0201e-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="0201e-326">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-327">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0201e-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-328">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-330">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="0201e-330">Provides high level status information.</span></span> <span data-ttu-id="0201e-331">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="0201e-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="0201e-332">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="0201e-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0201e-333">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0201e-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-335">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-337">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="0201e-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="0201e-338">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="0201e-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-339">**État**</span><span class="sxs-lookup"><span data-stu-id="0201e-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-342">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0201e-342">The current status of the object.</span></span> <span data-ttu-id="0201e-343">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-344">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0201e-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-345">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="0201e-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0201e-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-347">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0201e-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0201e-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="0201e-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0201e-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0201e-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-350">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-352">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="0201e-352">The current state of the logical device.</span></span> <span data-ttu-id="0201e-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0201e-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-357">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0201e-357">The scoping system's creation class name.</span></span> <span data-ttu-id="0201e-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="0201e-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0201e-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0201e-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0201e-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-362">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0201e-362">The scoping system's name.</span></span> <span data-ttu-id="0201e-363">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et est le nom du [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associé à ce service de pulsation.</span><span class="sxs-lookup"><span data-stu-id="0201e-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-364">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="0201e-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-365">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0201e-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-367">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0201e-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0201e-368">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0201e-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-369">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="0201e-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-370">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0201e-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-372">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0201e-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="0201e-373">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0201e-374">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="0201e-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0201e-375">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0201e-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0201e-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0201e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0201e-377">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="0201e-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0201e-378">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="0201e-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0201e-379">Notes</span><span class="sxs-lookup"><span data-stu-id="0201e-379">Remarks</span></span>

<span data-ttu-id="0201e-380">L’accès à la classe **MSVM \_ HeartbeatComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="0201e-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0201e-381">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0201e-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0201e-382">Exemples</span><span class="sxs-lookup"><span data-stu-id="0201e-382">Examples</span></span>

<span data-ttu-id="0201e-383">L’exemple C# suivant obtient l’état d’intégrité de l’application d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0201e-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="0201e-384">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0201e-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0201e-385">Pour fonctionner correctement, le code suivant doit être exécuté avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0201e-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="0201e-386">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0201e-386">Requirements</span></span>



| <span data-ttu-id="0201e-387">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0201e-387">Requirement</span></span> | <span data-ttu-id="0201e-388">Valeur</span><span class="sxs-lookup"><span data-stu-id="0201e-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0201e-389">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0201e-389">Minimum supported client</span></span><br/> | <span data-ttu-id="0201e-390">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0201e-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0201e-391">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0201e-391">Minimum supported server</span></span><br/> | <span data-ttu-id="0201e-392">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0201e-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0201e-393">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0201e-393">Namespace</span></span><br/>                | <span data-ttu-id="0201e-394">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0201e-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0201e-395">MOF</span><span class="sxs-lookup"><span data-stu-id="0201e-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0201e-396"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0201e-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0201e-397">DLL</span><span class="sxs-lookup"><span data-stu-id="0201e-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0201e-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0201e-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0201e-399">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0201e-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0201e-400">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0201e-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="0201e-401">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0201e-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="0201e-402">**MSVM \_ HeartbeatComponent**</span><span class="sxs-lookup"><span data-stu-id="0201e-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

