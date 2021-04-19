---
description: Représente les fonctionnalités et la gestion du contrôleur série.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Msvm_SerialController, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516923"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="5e06b-103">MSVM \_ SerialController, classe</span><span class="sxs-lookup"><span data-stu-id="5e06b-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="5e06b-104">Représente les fonctionnalités et la gestion du contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="5e06b-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="5e06b-105">Les contrôleurs série sont des périphériques logiques qui sont toujours présents dans un ordinateur virtuel, et ne sont donc pas alloués par le biais d’un pool de ressources.</span><span class="sxs-lookup"><span data-stu-id="5e06b-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="5e06b-106">Une instance de contrôleur série est toujours présente dans un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5e06b-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="5e06b-107">Les contrôleurs série ont un nombre fixe d’instances de port.</span><span class="sxs-lookup"><span data-stu-id="5e06b-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="5e06b-108">Cette implémentation prend en charge deux ports par contrôleur.</span><span class="sxs-lookup"><span data-stu-id="5e06b-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="5e06b-109">Les contrôleurs série sont facultatifs dans les [ordinateurs virtuels de génération 2](virtualization-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5e06b-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="5e06b-110">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5e06b-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e06b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e06b-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
  uint16   OperationalStatus[] = { 2 };
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
  string   CreationClassName = "Msvm_SerialController";
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="5e06b-112">Membres</span><span class="sxs-lookup"><span data-stu-id="5e06b-112">Members</span></span>

<span data-ttu-id="5e06b-113">La classe **MSVM \_ SerialController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5e06b-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="5e06b-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e06b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5e06b-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e06b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5e06b-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e06b-116">Methods</span></span>

<span data-ttu-id="5e06b-117">La classe **MSVM \_ SerialController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5e06b-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="5e06b-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="5e06b-118">Method</span></span>                                                                 | <span data-ttu-id="5e06b-119">Description</span><span class="sxs-lookup"><span data-stu-id="5e06b-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="5e06b-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="5e06b-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="5e06b-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e06b-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5e06b-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="5e06b-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="5e06b-123">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e06b-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5e06b-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="5e06b-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="5e06b-125">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e06b-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="5e06b-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5e06b-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="5e06b-127">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="5e06b-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="5e06b-128">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="5e06b-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="5e06b-129">Réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5e06b-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="5e06b-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="5e06b-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="5e06b-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e06b-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5e06b-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="5e06b-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="5e06b-133">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e06b-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5e06b-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5e06b-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="5e06b-135">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5e06b-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5e06b-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e06b-136">Properties</span></span>

<span data-ttu-id="5e06b-137">La classe **MSVM \_ SerialController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e06b-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e06b-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="5e06b-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-139">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-141">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5e06b-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="5e06b-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5e06b-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="5e06b-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-143">Value</span></span>                                                                            | <span data-ttu-id="5e06b-144">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5e06b-145"><dt>6,3</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="5e06b-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="5e06b-147">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5e06b-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-148">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="5e06b-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-151">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5e06b-151">The primary availability and status of the device.</span></span> <span data-ttu-id="5e06b-152">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5e06b-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="5e06b-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-153">Value</span></span>                                                                        | <span data-ttu-id="5e06b-154">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5e06b-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="5e06b-156">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5e06b-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-157">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5e06b-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-158">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-160">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5e06b-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5e06b-161">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="5e06b-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-163">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-165">La mise en mémoire tampon et d’autres fonctionnalités du contrôleur série qui peuvent être inhérentes au matériel de puce.</span><span class="sxs-lookup"><span data-stu-id="5e06b-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="5e06b-166">Cette propriété est héritée de la [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-167">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5e06b-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-168">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5e06b-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-170">Tableau de chaînes de forme libre qui fournit des explications plus détaillées sur les fonctionnalités du contrôleur série indiquées dans le tableau de **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="5e06b-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="5e06b-171">Cette propriété est héritée de la [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5e06b-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-175">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5e06b-175">A short description of the object.</span></span> <span data-ttu-id="5e06b-176">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5e06b-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-180">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="5e06b-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5e06b-181">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5e06b-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5e06b-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5e06b-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5e06b-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="5e06b-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="5e06b-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="5e06b-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5e06b-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5e06b-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5e06b-190">)</span><span class="sxs-lookup"><span data-stu-id="5e06b-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e06b-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e06b-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-194">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="5e06b-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5e06b-195">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5e06b-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-196">**Description**</span><span class="sxs-lookup"><span data-stu-id="5e06b-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-199">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="5e06b-199">A description of the object.</span></span> <span data-ttu-id="5e06b-200">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5e06b-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-204">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5e06b-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5e06b-205">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5e06b-206">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5e06b-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="5e06b-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="5e06b-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="5e06b-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="5e06b-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="5e06b-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="5e06b-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5e06b-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5e06b-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5e06b-215">)</span><span class="sxs-lookup"><span data-stu-id="5e06b-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e06b-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5e06b-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-219">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft : *<GUID>* ».</span><span class="sxs-lookup"><span data-stu-id="5e06b-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5e06b-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-223">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5e06b-223">A display name for the object.</span></span> <span data-ttu-id="5e06b-224">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-225">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5e06b-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-226">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-228">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5e06b-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5e06b-229">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e06b-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5e06b-230">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-230">Value</span></span>                                                                        | <span data-ttu-id="5e06b-231">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="5e06b-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5e06b-233">activé</span><span class="sxs-lookup"><span data-stu-id="5e06b-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5e06b-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-235">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-237">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="5e06b-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5e06b-238">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="5e06b-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5e06b-239">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e06b-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5e06b-240">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-240">Value</span></span>                                                                        | <span data-ttu-id="5e06b-241">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5e06b-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="5e06b-243">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5e06b-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-244">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5e06b-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-245">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5e06b-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-247">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="5e06b-248">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5e06b-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-250">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-252">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="5e06b-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="5e06b-253">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5e06b-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-255">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-257">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5e06b-257">The current health of the element.</span></span> <span data-ttu-id="5e06b-258">Cela exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="5e06b-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5e06b-259">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="5e06b-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5e06b-260">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5e06b-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-262">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5e06b-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-264">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="5e06b-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="5e06b-265">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5e06b-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5e06b-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-267">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e06b-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-269">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5e06b-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5e06b-270">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5e06b-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-274">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="5e06b-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-275">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5e06b-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5e06b-276">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5e06b-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-278">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e06b-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-280">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="5e06b-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="5e06b-281">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-282">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="5e06b-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e06b-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-285">Débit en bauds maximal, en bits par seconde, pris en charge par le contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="5e06b-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="5e06b-286">Cette propriété est héritée de la [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="5e06b-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-288">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e06b-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-290">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="5e06b-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="5e06b-291">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="5e06b-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="5e06b-292">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="5e06b-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="5e06b-293">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-294">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="5e06b-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-295">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e06b-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-297">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-297">This property has been deprecated.</span></span> <span data-ttu-id="5e06b-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-299">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5e06b-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-302">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="5e06b-302">The label by which the object is known.</span></span> <span data-ttu-id="5e06b-303">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="5e06b-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-304">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5e06b-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-305">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-307">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5e06b-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5e06b-308">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5e06b-309">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5e06b-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5e06b-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5e06b-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="5e06b-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="5e06b-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="5e06b-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="5e06b-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="5e06b-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="5e06b-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="5e06b-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="5e06b-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="5e06b-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="5e06b-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="5e06b-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="5e06b-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="5e06b-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="5e06b-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="5e06b-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5e06b-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5e06b-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5e06b-329">)</span><span class="sxs-lookup"><span data-stu-id="5e06b-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e06b-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5e06b-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-331">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-333">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5e06b-333">The current statuses of the object.</span></span> <span data-ttu-id="5e06b-334">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-335">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5e06b-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-338">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="5e06b-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5e06b-339">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="5e06b-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5e06b-340">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e06b-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5e06b-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-342">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5e06b-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-344">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="5e06b-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="5e06b-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5e06b-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5e06b-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-347">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-349">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5e06b-349">The power management capabilities of the device.</span></span> <span data-ttu-id="5e06b-350">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-351">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5e06b-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-352">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5e06b-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-354">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="5e06b-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="5e06b-355">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-356">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5e06b-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-357">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e06b-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-359">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="5e06b-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="5e06b-360">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-361">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5e06b-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-362">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-364">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="5e06b-364">Provides high level status information.</span></span> <span data-ttu-id="5e06b-365">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="5e06b-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5e06b-366">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5e06b-367">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5e06b-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="5e06b-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="5e06b-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="5e06b-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="5e06b-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5e06b-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5e06b-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5e06b-374">)</span><span class="sxs-lookup"><span data-stu-id="5e06b-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5e06b-375">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="5e06b-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-378">Chaîne qui fournit des informations supplémentaires relatives au protocole pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="5e06b-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="5e06b-379">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-380">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="5e06b-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-381">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-383">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="5e06b-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="5e06b-384">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="5e06b-385">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-385">Value</span></span>                                                                         | <span data-ttu-id="5e06b-386">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="5e06b-387"><dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="5e06b-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="5e06b-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5e06b-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-390">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-392">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="5e06b-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="5e06b-393">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5e06b-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5e06b-394">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="5e06b-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="5e06b-395">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e06b-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5e06b-396">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-396">Value</span></span>                                                                         | <span data-ttu-id="5e06b-397">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5e06b-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="5e06b-399">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5e06b-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-400">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="5e06b-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-401">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-403">La sécurité opérationnelle pour le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="5e06b-403">The operational security for the controller.</span></span> <span data-ttu-id="5e06b-404">Cette propriété est héritée de la [**\_ SerialController CIM**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="5e06b-405">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-405">Value</span></span>                                                                        | <span data-ttu-id="5e06b-406">Signification</span><span class="sxs-lookup"><span data-stu-id="5e06b-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="5e06b-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="5e06b-408">Aucun</span><span class="sxs-lookup"><span data-stu-id="5e06b-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e06b-409">**État**</span><span class="sxs-lookup"><span data-stu-id="5e06b-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-410">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-412">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5e06b-412">The current status of the object.</span></span> <span data-ttu-id="5e06b-413">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-414">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5e06b-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-415">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="5e06b-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-417">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5e06b-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5e06b-418">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5e06b-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5e06b-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-420">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-422">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="5e06b-422">The current state of the logical device.</span></span> <span data-ttu-id="5e06b-423">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-424">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5e06b-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-425">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-427">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5e06b-427">The scoping system's creation class name.</span></span> <span data-ttu-id="5e06b-428">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5e06b-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-429">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5e06b-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e06b-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-432">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5e06b-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="5e06b-433">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5e06b-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-434">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5e06b-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-435">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e06b-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-437">La dernière fois que le contrôleur a été mis sous tension.</span><span class="sxs-lookup"><span data-stu-id="5e06b-437">The last time the controller was powered on.</span></span> <span data-ttu-id="5e06b-438">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="5e06b-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-439">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5e06b-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-440">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5e06b-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-441">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-442">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="5e06b-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5e06b-443">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="5e06b-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-444">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5e06b-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-445">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5e06b-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-447">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="5e06b-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="5e06b-448">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5e06b-449">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5e06b-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e06b-450">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5e06b-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5e06b-451">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e06b-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5e06b-452">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="5e06b-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5e06b-453">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="5e06b-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e06b-454">Notes</span><span class="sxs-lookup"><span data-stu-id="5e06b-454">Remarks</span></span>

<span data-ttu-id="5e06b-455">L’accès à la classe **MSVM \_ SerialController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="5e06b-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5e06b-456">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5e06b-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e06b-457">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e06b-457">Requirements</span></span>



| <span data-ttu-id="5e06b-458">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e06b-458">Requirement</span></span> | <span data-ttu-id="5e06b-459">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e06b-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e06b-460">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e06b-460">Minimum supported client</span></span><br/> | <span data-ttu-id="5e06b-461">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e06b-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e06b-462">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e06b-462">Minimum supported server</span></span><br/> | <span data-ttu-id="5e06b-463">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e06b-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e06b-464">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5e06b-464">Namespace</span></span><br/>                | <span data-ttu-id="5e06b-465">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5e06b-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e06b-466">MOF</span><span class="sxs-lookup"><span data-stu-id="5e06b-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e06b-467"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e06b-468">DLL</span><span class="sxs-lookup"><span data-stu-id="5e06b-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e06b-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e06b-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e06b-470">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e06b-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e06b-471">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="5e06b-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="5e06b-472">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="5e06b-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="5e06b-473">Classes d’appareils série</span><span class="sxs-lookup"><span data-stu-id="5e06b-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

