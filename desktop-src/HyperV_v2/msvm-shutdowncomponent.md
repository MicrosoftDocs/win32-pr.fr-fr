---
description: Représente l’état du service d’arrêt, qui fournit un mécanisme permettant d’arrêter le système d’exploitation de l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte.
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034202"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="4398e-103">MSVM \_ ShutdownComponent, classe</span><span class="sxs-lookup"><span data-stu-id="4398e-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="4398e-104">Représente l’état du service d’arrêt, qui fournit un mécanisme permettant d’arrêter le système d’exploitation de l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte.</span><span class="sxs-lookup"><span data-stu-id="4398e-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="4398e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4398e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4398e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4398e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_ShutdownComponent";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
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

## <a name="members"></a><span data-ttu-id="4398e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4398e-107">Members</span></span>

<span data-ttu-id="4398e-108">La classe **MSVM \_ ShutdownComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4398e-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4398e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4398e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4398e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4398e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4398e-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4398e-111">Methods</span></span>

<span data-ttu-id="4398e-112">La classe **MSVM \_ ShutdownComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4398e-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="4398e-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="4398e-113">Method</span></span>                                                                  | <span data-ttu-id="4398e-114">Description</span><span class="sxs-lookup"><span data-stu-id="4398e-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4398e-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4398e-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="4398e-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4398e-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="4398e-117">**InitiateReboot**</span><span class="sxs-lookup"><span data-stu-id="4398e-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="4398e-118">Lance une opération de redémarrage du système d’exploitation sur l’ordinateur virtuel enfant associé.</span><span class="sxs-lookup"><span data-stu-id="4398e-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="4398e-119">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="4398e-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="4398e-120">Lance une opération d’arrêt du système d’exploitation sur l’ordinateur virtuel enfant associé.</span><span class="sxs-lookup"><span data-stu-id="4398e-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="4398e-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="4398e-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="4398e-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4398e-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="4398e-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="4398e-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="4398e-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4398e-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="4398e-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4398e-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="4398e-126">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="4398e-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="4398e-127">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="4398e-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="4398e-128">Réinitialise le composant.</span><span class="sxs-lookup"><span data-stu-id="4398e-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="4398e-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="4398e-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="4398e-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4398e-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="4398e-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="4398e-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="4398e-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4398e-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="4398e-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4398e-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="4398e-134">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4398e-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="4398e-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4398e-135">Properties</span></span>

<span data-ttu-id="4398e-136">La classe **MSVM \_ ShutdownComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4398e-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4398e-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="4398e-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-138">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-140">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4398e-140">Additional availability and status of the device.</span></span> <span data-ttu-id="4398e-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4398e-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="4398e-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-142">Value</span></span>                                                                        | <span data-ttu-id="4398e-143">Signification</span><span class="sxs-lookup"><span data-stu-id="4398e-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4398e-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="4398e-145">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4398e-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4398e-146">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="4398e-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-149">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4398e-149">The primary availability and status of the device.</span></span> <span data-ttu-id="4398e-150">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="4398e-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-151">Value</span></span>                                                                        | <span data-ttu-id="4398e-152">Signification</span><span class="sxs-lookup"><span data-stu-id="4398e-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4398e-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="4398e-154">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4398e-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4398e-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4398e-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-156">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-158">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4398e-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4398e-159">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4398e-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-163">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4398e-163">A short description of the object.</span></span> <span data-ttu-id="4398e-164">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4398e-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-166">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-168">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4398e-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4398e-169">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4398e-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4398e-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4398e-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4398e-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4398e-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="4398e-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="4398e-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="4398e-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4398e-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4398e-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4398e-178">)</span><span class="sxs-lookup"><span data-stu-id="4398e-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4398e-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4398e-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-182">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4398e-182">The scoping system's creation class name.</span></span> <span data-ttu-id="4398e-183">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4398e-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-184">**Description**</span><span class="sxs-lookup"><span data-stu-id="4398e-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-187">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="4398e-187">A description of the object.</span></span> <span data-ttu-id="4398e-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4398e-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-192">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4398e-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4398e-193">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4398e-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4398e-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4398e-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="4398e-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="4398e-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="4398e-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="4398e-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="4398e-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="4398e-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4398e-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4398e-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4398e-203">)</span><span class="sxs-lookup"><span data-stu-id="4398e-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4398e-204">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4398e-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-205">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-207">Une adresse ou d’autres informations d’identification pour nommer de manière unique le LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="4398e-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="4398e-208">Cette propriété est héritée [**de CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*VMGUID* \\ *GUID*», où *VMGUID* est la propriété **Name** de l’instance [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associée à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4398e-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4398e-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-212">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4398e-212">A display name for the object.</span></span> <span data-ttu-id="4398e-213">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-214">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4398e-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-215">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-217">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4398e-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="4398e-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-218">Value</span></span>                                                                        | <span data-ttu-id="4398e-219">Signification</span><span class="sxs-lookup"><span data-stu-id="4398e-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="4398e-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="4398e-221">Pas de valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="4398e-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4398e-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4398e-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-225">État activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4398e-225">The enabled state of the element.</span></span> <span data-ttu-id="4398e-226">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et a la valeur 2 (activé) ou 3 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="4398e-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="4398e-227">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-227">Value</span></span>                                                                        | <span data-ttu-id="4398e-228">Signification</span><span class="sxs-lookup"><span data-stu-id="4398e-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4398e-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4398e-230">activé</span><span class="sxs-lookup"><span data-stu-id="4398e-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="4398e-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="4398e-232">Désactivé</span><span class="sxs-lookup"><span data-stu-id="4398e-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4398e-233">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4398e-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-234">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4398e-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-236">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="4398e-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="4398e-237">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4398e-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-239">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-241">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="4398e-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="4398e-242">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4398e-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-244">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-246">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4398e-246">The current health of the element.</span></span> <span data-ttu-id="4398e-247">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="4398e-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4398e-248">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4398e-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-250">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4398e-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-252">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="4398e-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="4398e-253">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4398e-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-255">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4398e-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-257">Date et heure auxquelles le service d’intégration a été installé sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4398e-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="4398e-258">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4398e-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-260">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4398e-262">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4398e-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4398e-263">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4398e-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4398e-264">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-265">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4398e-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-266">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4398e-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-268">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4398e-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="4398e-269">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-270">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="4398e-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-271">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4398e-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-273">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="4398e-273">This property has been deprecated.</span></span> <span data-ttu-id="4398e-274">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4398e-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-275">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4398e-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-278">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4398e-278">The label by which the object is known.</span></span> <span data-ttu-id="4398e-279">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-280">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4398e-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-281">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-283">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4398e-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4398e-284">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4398e-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4398e-285">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4398e-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4398e-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4398e-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="4398e-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="4398e-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="4398e-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="4398e-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="4398e-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="4398e-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="4398e-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="4398e-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="4398e-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="4398e-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="4398e-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="4398e-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="4398e-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="4398e-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="4398e-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4398e-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4398e-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4398e-305">)</span><span class="sxs-lookup"><span data-stu-id="4398e-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4398e-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4398e-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-307">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-309">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4398e-309">The current status of the element.</span></span> <span data-ttu-id="4398e-310">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="4398e-311">Les valeurs possibles pour la valeur de la propriété **OperationalStatus** 0 sont les suivantes \[ \] .</span><span class="sxs-lookup"><span data-stu-id="4398e-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="4398e-312">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="4398e-313">Signification</span><span class="sxs-lookup"><span data-stu-id="4398e-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="4398e-314"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="4398e-315">Le service fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="4398e-315">The service is operating normally.</span></span> <span data-ttu-id="4398e-316">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4398e-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="4398e-317"><dt>**Dégradé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="4398e-318">Le service fonctionne normalement, mais le service invité a négocié une version de protocole de communication compatible.</span><span class="sxs-lookup"><span data-stu-id="4398e-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="4398e-319">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4398e-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="4398e-320"><dt>**Erreur non récupérable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="4398e-321">L’invité ne prend pas en charge une version de protocole compatible.</span><span class="sxs-lookup"><span data-stu-id="4398e-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="4398e-322">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="4398e-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="4398e-323"><dt>**Aucun contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="4398e-324">Le service invité n’est pas installé ou n’a pas encore été contacté.</span><span class="sxs-lookup"><span data-stu-id="4398e-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="4398e-325"><dt>**Communication perdue**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="4398e-326">Le service invité ne répond plus normalement.</span><span class="sxs-lookup"><span data-stu-id="4398e-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="4398e-327">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4398e-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-330">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4398e-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4398e-331">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="4398e-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="4398e-332">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4398e-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4398e-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-334">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4398e-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-336">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="4398e-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4398e-337">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et prend toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="4398e-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4398e-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-339">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-341">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4398e-341">The power management capabilities of the device.</span></span> <span data-ttu-id="4398e-342">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4398e-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-344">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4398e-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-346">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4398e-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="4398e-347">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-348">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4398e-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-349">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4398e-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-351">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4398e-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="4398e-352">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4398e-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-354">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-356">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="4398e-356">Provides high level status information.</span></span> <span data-ttu-id="4398e-357">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="4398e-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4398e-358">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4398e-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4398e-359">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4398e-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4398e-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4398e-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="4398e-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="4398e-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4398e-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4398e-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4398e-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4398e-366">)</span><span class="sxs-lookup"><span data-stu-id="4398e-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4398e-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4398e-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-368">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-370">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="4398e-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="4398e-371">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="4398e-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4398e-372">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="4398e-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="4398e-373">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="4398e-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="4398e-374">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-374">Value</span></span>                                                                         | <span data-ttu-id="4398e-375">Signification</span><span class="sxs-lookup"><span data-stu-id="4398e-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="4398e-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4398e-377">Non applicable</span><span class="sxs-lookup"><span data-stu-id="4398e-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4398e-378">**État**</span><span class="sxs-lookup"><span data-stu-id="4398e-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-381">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4398e-381">The current status of the object.</span></span> <span data-ttu-id="4398e-382">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4398e-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-384">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4398e-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4398e-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-386">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4398e-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4398e-387">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4398e-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4398e-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-389">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-391">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4398e-391">The current state of the logical device.</span></span> <span data-ttu-id="4398e-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4398e-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-396">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4398e-396">The scoping system's creation class name.</span></span> <span data-ttu-id="4398e-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4398e-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4398e-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-399">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4398e-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-401">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4398e-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="4398e-402">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4398e-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4398e-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-404">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4398e-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-406">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4398e-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4398e-407">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4398e-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4398e-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4398e-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-409">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4398e-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-411">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4398e-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4398e-412">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4398e-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4398e-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4398e-414">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4398e-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4398e-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4398e-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4398e-416">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="4398e-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4398e-417">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4398e-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4398e-418">Notes</span><span class="sxs-lookup"><span data-stu-id="4398e-418">Remarks</span></span>

<span data-ttu-id="4398e-419">L’accès à la classe **MSVM \_ ShutdownComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4398e-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4398e-420">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4398e-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4398e-421">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4398e-421">Requirements</span></span>



| <span data-ttu-id="4398e-422">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4398e-422">Requirement</span></span> | <span data-ttu-id="4398e-423">Valeur</span><span class="sxs-lookup"><span data-stu-id="4398e-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4398e-424">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4398e-424">Minimum supported client</span></span><br/> | <span data-ttu-id="4398e-425">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4398e-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4398e-426">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4398e-426">Minimum supported server</span></span><br/> | <span data-ttu-id="4398e-427">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4398e-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4398e-428">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4398e-428">Namespace</span></span><br/>                | <span data-ttu-id="4398e-429">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4398e-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4398e-430">MOF</span><span class="sxs-lookup"><span data-stu-id="4398e-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4398e-431"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4398e-432">DLL</span><span class="sxs-lookup"><span data-stu-id="4398e-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4398e-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4398e-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4398e-434">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4398e-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4398e-435">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4398e-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="4398e-436">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4398e-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

