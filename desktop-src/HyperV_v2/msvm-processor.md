---
description: Représente le processeur virtuel sur un ordinateur virtuel.
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Msvm_Processor, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865529"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="4e732-103">\_Classe de processeur MSVM</span><span class="sxs-lookup"><span data-stu-id="4e732-103">Msvm\_Processor class</span></span>

<span data-ttu-id="4e732-104">Représente le processeur virtuel sur un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="4e732-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4e732-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e732-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e732-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
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
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="4e732-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4e732-107">Members</span></span>

<span data-ttu-id="4e732-108">La classe de **\_ processeur MSVM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4e732-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="4e732-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4e732-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e732-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4e732-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e732-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4e732-111">Methods</span></span>

<span data-ttu-id="4e732-112">La classe de **\_ processeur MSVM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4e732-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="4e732-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="4e732-113">Method</span></span>                                                          | <span data-ttu-id="4e732-114">Description</span><span class="sxs-lookup"><span data-stu-id="4e732-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="4e732-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4e732-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="4e732-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e732-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4e732-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="4e732-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="4e732-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e732-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4e732-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="4e732-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="4e732-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e732-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="4e732-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4e732-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="4e732-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="4e732-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="4e732-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="4e732-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="4e732-124">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="4e732-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="4e732-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="4e732-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e732-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4e732-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="4e732-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="4e732-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e732-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4e732-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4e732-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="4e732-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e732-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e732-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4e732-131">Properties</span></span>

<span data-ttu-id="4e732-132">La classe du **\_ processeur MSVM** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4e732-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e732-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="4e732-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-136">Disponibilité et état supplémentaires de l’appareil, au-delà de celui spécifié dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="4e732-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="4e732-137">La propriété de **disponibilité** indique l’état principal et la disponibilité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e732-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="4e732-138">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4e732-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-139">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="4e732-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-140">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-142">Largeur d’adresse du processeur, en bits.</span><span class="sxs-lookup"><span data-stu-id="4e732-142">The processor address width, in bits.</span></span> <span data-ttu-id="4e732-143">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor)et la valeur est 32 ou 64, selon les caractéristiques de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4e732-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-144">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="4e732-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-147">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e732-147">The primary availability and status of the device.</span></span> <span data-ttu-id="4e732-148">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-149">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4e732-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-150">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-152">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4e732-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4e732-153">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4e732-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4e732-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-157">Qualificateurs : **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4e732-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4e732-158">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e732-158">A short description of the object.</span></span> <span data-ttu-id="4e732-159">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-160">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4e732-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-163">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4e732-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4e732-164">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4e732-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4e732-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4e732-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4e732-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4e732-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="4e732-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="4e732-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="4e732-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4e732-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4e732-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4e732-173">)</span><span class="sxs-lookup"><span data-stu-id="4e732-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e732-174">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="4e732-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-175">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-177">État actuel du processeur.</span><span class="sxs-lookup"><span data-stu-id="4e732-177">The current status of the processor.</span></span> <span data-ttu-id="4e732-178">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e732-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-182">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4e732-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e732-183">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="4e732-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4e732-184">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de la classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="4e732-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="4e732-185">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4e732-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-186">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="4e732-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-187">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e732-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-189">Vitesse maximale du processeur physique, en tenant compte de la capacité du processeur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="4e732-190">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="4e732-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-192">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-194">Largeur des données du processeur, en bits.</span><span class="sxs-lookup"><span data-stu-id="4e732-194">The processor data width, in bits.</span></span> <span data-ttu-id="4e732-195">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor)et la valeur est 32 ou 64, selon les caractéristiques de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4e732-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-196">**Description**</span><span class="sxs-lookup"><span data-stu-id="4e732-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-199">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="4e732-199">A description of the object.</span></span> <span data-ttu-id="4e732-200">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4e732-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-204">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4e732-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4e732-205">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4e732-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4e732-206">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4e732-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="4e732-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="4e732-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="4e732-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="4e732-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="4e732-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="4e732-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4e732-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4e732-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4e732-215">)</span><span class="sxs-lookup"><span data-stu-id="4e732-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e732-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4e732-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-219">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4e732-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="4e732-220">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID* \\ *Device Specific Data*».</span><span class="sxs-lookup"><span data-stu-id="4e732-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="4e732-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4e732-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-224">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e732-224">A display name for the object.</span></span> <span data-ttu-id="4e732-225">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-226">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4e732-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-227">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-229">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4e732-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="4e732-230">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e732-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4e732-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-232">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-234">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4e732-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4e732-235">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e732-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-236">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4e732-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-237">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4e732-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-239">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="4e732-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="4e732-240">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4e732-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-244">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="4e732-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="4e732-245">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-246">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="4e732-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-247">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e732-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-249">La vitesse d’horloge du bus externe du processeur physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4e732-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="4e732-250">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-251">**Famille**</span><span class="sxs-lookup"><span data-stu-id="4e732-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-252">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-254">Famille de processeurs du processeur physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4e732-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="4e732-255">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4e732-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-259">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4e732-259">The current health of the element.</span></span> <span data-ttu-id="4e732-260">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4e732-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-262">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4e732-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-264">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="4e732-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="4e732-265">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4e732-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e732-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-267">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e732-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-269">Date et heure de création de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4e732-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="4e732-270">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4e732-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-274">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4e732-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4e732-275">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4e732-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4e732-276">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4e732-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-278">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e732-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-280">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4e732-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="4e732-281">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-282">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="4e732-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-285">Pourcentage actuel de la puissance de traitement totale consommée par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="4e732-286">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-287">**LoadPercentageHistory**</span><span class="sxs-lookup"><span data-stu-id="4e732-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-288">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-290">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="4e732-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4e732-291">Historique enregistré du pourcentage de la puissance de traitement totale consommée par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="4e732-292">Il s’agit d’un tableau contenant des exemples.</span><span class="sxs-lookup"><span data-stu-id="4e732-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="4e732-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-294">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e732-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-296">Vitesse d’horloge maximale, en mégahertz, du processeur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="4e732-297">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-298">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="4e732-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-299">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e732-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-301">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="4e732-301">This property has been deprecated.</span></span> <span data-ttu-id="4e732-302">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-303">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4e732-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-306">Qualificateurs : **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="4e732-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4e732-307">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4e732-307">The label by which the object is known.</span></span> <span data-ttu-id="4e732-308">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="4e732-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="4e732-309">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-310">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4e732-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-311">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-313">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4e732-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4e732-314">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4e732-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4e732-315">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4e732-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4e732-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4e732-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="4e732-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="4e732-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="4e732-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="4e732-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="4e732-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="4e732-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="4e732-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="4e732-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="4e732-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="4e732-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="4e732-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="4e732-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="4e732-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="4e732-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="4e732-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4e732-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4e732-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4e732-335">)</span><span class="sxs-lookup"><span data-stu-id="4e732-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e732-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4e732-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-337">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-339">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4e732-339">The current status of the element.</span></span> <span data-ttu-id="4e732-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-341">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4e732-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-344">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4e732-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4e732-345">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="4e732-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4e732-346">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e732-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-347">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="4e732-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-350">Description du type de la famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="4e732-350">A description of the processor family type.</span></span> <span data-ttu-id="4e732-351">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4e732-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4e732-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-353">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4e732-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-355">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="4e732-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="4e732-356">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4e732-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4e732-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-358">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-359">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-360">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e732-360">The power management capabilities of the device.</span></span> <span data-ttu-id="4e732-361">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-362">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4e732-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-363">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4e732-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-364">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-365">Indique si la gestion de l’alimentation est prise en charge sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4e732-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="4e732-366">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-367">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4e732-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-368">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e732-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-370">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="4e732-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="4e732-371">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-372">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4e732-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-373">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-375">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="4e732-375">Provides high level status information.</span></span> <span data-ttu-id="4e732-376">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="4e732-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4e732-377">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4e732-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4e732-378">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4e732-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4e732-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4e732-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="4e732-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="4e732-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4e732-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4e732-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4e732-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4e732-385">)</span><span class="sxs-lookup"><span data-stu-id="4e732-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e732-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4e732-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-389">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="4e732-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="4e732-390">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e732-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-391">**Rôle**</span><span class="sxs-lookup"><span data-stu-id="4e732-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-392">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-394">Chaîne qui décrit le rôle du processeur.</span><span class="sxs-lookup"><span data-stu-id="4e732-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="4e732-395">Par exemple, « processeur central » ou « processeur mathématique ».</span><span class="sxs-lookup"><span data-stu-id="4e732-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="4e732-396">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-397">**État**</span><span class="sxs-lookup"><span data-stu-id="4e732-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-400">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e732-400">The current status of the object.</span></span> <span data-ttu-id="4e732-401">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-402">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4e732-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-403">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4e732-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e732-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-405">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4e732-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4e732-406">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4e732-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4e732-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-408">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-410">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="4e732-410">The current state of the logical device.</span></span> <span data-ttu-id="4e732-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-412">**Exécution pas à pas**</span><span class="sxs-lookup"><span data-stu-id="4e732-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-413">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-415">Niveau de révision du processeur au sein de la famille de processeurs du processeur physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4e732-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="4e732-416">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e732-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-420">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4e732-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e732-421">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4e732-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="4e732-422">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4e732-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4e732-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e732-426">Qualificateurs : **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4e732-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e732-427">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4e732-427">The name of the scoping system.</span></span> <span data-ttu-id="4e732-428">Cette valeur correspond à la valeur de la propriété [**Name**](msvm-computersystem.md) de la classe **MSVM \_ ComputerSystem** pour l’ordinateur virtuel d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4e732-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="4e732-429">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4e732-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-430">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4e732-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-431">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e732-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-433">Date ou heure de modification de l’état de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4e732-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="4e732-434">Si l’état de l’élément n’a pas été modifié et que cette propriété est remplie, elle doit être définie sur une valeur d’intervalle 0.</span><span class="sxs-lookup"><span data-stu-id="4e732-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="4e732-435">Si une modification d’État a été demandée, mais rejetée ou n’a pas encore été traitée, la propriété ne doit pas être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4e732-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="4e732-436">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4e732-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4e732-437">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4e732-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-438">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4e732-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-439">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-440">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="4e732-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="4e732-441">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-442">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4e732-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-443">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-444">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-445">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="4e732-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4e732-446">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4e732-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-447">**Quei**</span><span class="sxs-lookup"><span data-stu-id="4e732-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e732-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-450">Identificateur global unique du processeur.</span><span class="sxs-lookup"><span data-stu-id="4e732-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="4e732-451">Cet identificateur peut uniquement être unique au sein d’une famille de processeurs.</span><span class="sxs-lookup"><span data-stu-id="4e732-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="4e732-452">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4e732-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4e732-453">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="4e732-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e732-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e732-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e732-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e732-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e732-456">Les informations de socket de l’UC, qui incluent des données sur la mise à niveau du processeur (si les mises à niveau sont prises en charge).</span><span class="sxs-lookup"><span data-stu-id="4e732-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="4e732-457">Cette propriété est héritée [**du \_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="4e732-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e732-458">Notes</span><span class="sxs-lookup"><span data-stu-id="4e732-458">Remarks</span></span>

<span data-ttu-id="4e732-459">L’accès à la classe de **\_ processeur MSVM** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4e732-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4e732-460">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4e732-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e732-461">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e732-461">Requirements</span></span>



| <span data-ttu-id="4e732-462">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e732-462">Requirement</span></span> | <span data-ttu-id="4e732-463">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e732-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e732-464">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e732-464">Minimum supported client</span></span><br/> | <span data-ttu-id="4e732-465">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e732-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4e732-466">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e732-466">Minimum supported server</span></span><br/> | <span data-ttu-id="4e732-467">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e732-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e732-468">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4e732-468">Namespace</span></span><br/>                | <span data-ttu-id="4e732-469">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4e732-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4e732-470">MOF</span><span class="sxs-lookup"><span data-stu-id="4e732-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e732-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e732-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e732-472">DLL</span><span class="sxs-lookup"><span data-stu-id="4e732-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e732-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e732-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e732-474">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e732-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e732-475">**\_Processeur CIM**</span><span class="sxs-lookup"><span data-stu-id="4e732-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="4e732-476">**\_Processeur CIM**</span><span class="sxs-lookup"><span data-stu-id="4e732-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="4e732-477">Classes de processeur</span><span class="sxs-lookup"><span data-stu-id="4e732-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

