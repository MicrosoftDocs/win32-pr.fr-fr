---
description: Représente un port série associé au contrôleur série.
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Classe Msvm_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865514"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="6972a-103">MSVM \_ SerialPort (classe)</span><span class="sxs-lookup"><span data-stu-id="6972a-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="6972a-104">Représente un port série associé au contrôleur série.</span><span class="sxs-lookup"><span data-stu-id="6972a-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="6972a-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="6972a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6972a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6972a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_SerialPort";
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
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="6972a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="6972a-107">Members</span></span>

<span data-ttu-id="6972a-108">La classe **MSVM \_ SerialPort** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6972a-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="6972a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6972a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6972a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6972a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6972a-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6972a-111">Methods</span></span>

<span data-ttu-id="6972a-112">La classe **MSVM \_ SerialPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6972a-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="6972a-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="6972a-113">Method</span></span>                                                           | <span data-ttu-id="6972a-114">Description</span><span class="sxs-lookup"><span data-stu-id="6972a-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="6972a-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="6972a-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="6972a-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6972a-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6972a-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="6972a-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="6972a-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6972a-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6972a-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="6972a-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="6972a-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6972a-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="6972a-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6972a-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="6972a-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="6972a-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="6972a-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="6972a-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="6972a-124">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="6972a-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="6972a-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="6972a-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="6972a-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6972a-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6972a-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="6972a-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="6972a-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6972a-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="6972a-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6972a-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="6972a-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6972a-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6972a-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6972a-131">Properties</span></span>

<span data-ttu-id="6972a-132">La classe **MSVM \_ SerialPort** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="6972a-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6972a-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="6972a-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-136">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6972a-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="6972a-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6972a-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="6972a-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-138">Value</span></span>                                                                            | <span data-ttu-id="6972a-139">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6972a-140"><dt>6,3</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="6972a-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="6972a-142">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6972a-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6972a-143">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="6972a-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-146">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6972a-146">The primary availability and status of the device.</span></span> <span data-ttu-id="6972a-147">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6972a-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="6972a-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-148">Value</span></span>                                                                        | <span data-ttu-id="6972a-149">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6972a-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="6972a-151">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6972a-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6972a-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6972a-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-153">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-155">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="6972a-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="6972a-156">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6972a-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-160">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6972a-160">A short description of the object.</span></span> <span data-ttu-id="6972a-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6972a-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-165">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="6972a-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6972a-166">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6972a-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6972a-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6972a-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6972a-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="6972a-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="6972a-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="6972a-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="6972a-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6972a-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6972a-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6972a-175">)</span><span class="sxs-lookup"><span data-stu-id="6972a-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6972a-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6972a-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-179">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="6972a-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6972a-180">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6972a-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-181">**Description**</span><span class="sxs-lookup"><span data-stu-id="6972a-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-184">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="6972a-184">A description of the object.</span></span> <span data-ttu-id="6972a-185">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6972a-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-189">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6972a-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6972a-190">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6972a-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6972a-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6972a-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="6972a-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="6972a-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="6972a-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="6972a-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="6972a-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="6972a-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6972a-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6972a-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6972a-200">)</span><span class="sxs-lookup"><span data-stu-id="6972a-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6972a-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6972a-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-204">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*», où les *données spécifiques* à l’appareil sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="6972a-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6972a-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-208">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6972a-208">A display name for the object.</span></span> <span data-ttu-id="6972a-209">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6972a-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-211">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-213">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="6972a-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6972a-214">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="6972a-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-215">Value</span></span>                                                                        | <span data-ttu-id="6972a-216">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="6972a-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6972a-218">activé</span><span class="sxs-lookup"><span data-stu-id="6972a-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6972a-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6972a-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-220">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-222">État activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6972a-222">The enabled state of the element.</span></span> <span data-ttu-id="6972a-223">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="6972a-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6972a-224">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="6972a-225">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-225">Value</span></span>                                                                        | <span data-ttu-id="6972a-226">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6972a-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="6972a-228">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6972a-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6972a-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6972a-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-230">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6972a-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-232">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="6972a-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="6972a-233">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6972a-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-237">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="6972a-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="6972a-238">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6972a-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-240">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-242">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6972a-242">The current health of the element.</span></span> <span data-ttu-id="6972a-243">Cela exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="6972a-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6972a-244">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="6972a-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6972a-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6972a-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-247">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="6972a-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-249">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="6972a-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="6972a-250">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="6972a-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6972a-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-252">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6972a-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-254">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6972a-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6972a-255">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6972a-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6972a-259">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="6972a-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6972a-260">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="6972a-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6972a-261">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6972a-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-263">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6972a-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-265">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6972a-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="6972a-266">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-267">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="6972a-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-268">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6972a-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-270">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="6972a-270">This property has been deprecated.</span></span> <span data-ttu-id="6972a-271">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6972a-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-272">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="6972a-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-273">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6972a-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-275">Bande passante maximale du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6972a-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="6972a-276">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-277">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6972a-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-280">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="6972a-280">The label by which the object is known.</span></span> <span data-ttu-id="6972a-281">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="6972a-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6972a-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-285">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6972a-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6972a-286">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6972a-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6972a-287">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6972a-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6972a-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="6972a-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="6972a-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="6972a-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="6972a-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="6972a-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="6972a-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="6972a-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="6972a-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="6972a-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="6972a-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="6972a-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="6972a-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="6972a-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="6972a-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="6972a-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="6972a-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6972a-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6972a-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6972a-307">)</span><span class="sxs-lookup"><span data-stu-id="6972a-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6972a-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6972a-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-309">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-311">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6972a-311">The current statuses of the object.</span></span> <span data-ttu-id="6972a-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6972a-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-316">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="6972a-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="6972a-317">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="6972a-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6972a-318">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="6972a-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-320">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="6972a-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-322">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="6972a-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="6972a-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="6972a-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-324">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="6972a-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-327">Type de module, lorsque **portType** a la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="6972a-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="6972a-328">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="6972a-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-330">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-332">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="6972a-333">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-333">Value</span></span>                                                                        | <span data-ttu-id="6972a-334">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="6972a-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6972a-336">Autres</span><span class="sxs-lookup"><span data-stu-id="6972a-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6972a-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6972a-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-338">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-340">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6972a-340">The power management capabilities of the device.</span></span> <span data-ttu-id="6972a-341">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6972a-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-343">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6972a-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-345">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="6972a-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="6972a-346">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-347">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="6972a-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-348">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6972a-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-350">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="6972a-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="6972a-351">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-352">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6972a-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-353">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-354">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-355">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="6972a-355">Provides high level status information.</span></span> <span data-ttu-id="6972a-356">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="6972a-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6972a-357">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6972a-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6972a-358">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6972a-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="6972a-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="6972a-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="6972a-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="6972a-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="6972a-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6972a-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="6972a-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6972a-365">)</span><span class="sxs-lookup"><span data-stu-id="6972a-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6972a-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="6972a-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-367">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6972a-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-369">Bande passante demandée du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6972a-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="6972a-370">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6972a-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-372">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-374">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="6972a-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="6972a-375">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="6972a-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="6972a-376">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="6972a-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="6972a-377">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="6972a-378">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-378">Value</span></span>                                                                         | <span data-ttu-id="6972a-379">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6972a-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="6972a-381">Non applicable</span><span class="sxs-lookup"><span data-stu-id="6972a-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6972a-382">**Vitesse**</span><span class="sxs-lookup"><span data-stu-id="6972a-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-383">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6972a-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-385">Bande passante du port, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="6972a-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="6972a-386">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-387">**État**</span><span class="sxs-lookup"><span data-stu-id="6972a-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-390">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6972a-390">The current status of the object.</span></span> <span data-ttu-id="6972a-391">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-392">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6972a-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-393">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="6972a-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6972a-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-395">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="6972a-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6972a-396">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6972a-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6972a-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-398">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-400">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="6972a-400">The current state of the logical device.</span></span> <span data-ttu-id="6972a-401">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6972a-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-405">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6972a-405">The scoping system's creation class name.</span></span> <span data-ttu-id="6972a-406">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6972a-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6972a-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-408">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6972a-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-410">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="6972a-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="6972a-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="6972a-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="6972a-412">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6972a-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-413">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6972a-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-415">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6972a-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6972a-416">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="6972a-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-417">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="6972a-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-418">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6972a-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-420">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="6972a-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="6972a-421">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-422">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6972a-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-423">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-425">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="6972a-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6972a-426">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="6972a-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6972a-427">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="6972a-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6972a-428">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6972a-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6972a-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6972a-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6972a-430">Dans certains cas, un port logique peut être identifiable comme un port frontal ou back end.</span><span class="sxs-lookup"><span data-stu-id="6972a-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="6972a-431">C’est le cas, par exemple, d’un groupe de stockage qui peut avoir back end ports pour communiquer avec les lecteurs de disque et les ports frontaux pour communiquer avec les hôtes.</span><span class="sxs-lookup"><span data-stu-id="6972a-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="6972a-432">S’il n’existe aucune restriction sur l’utilisation du port, la valeur doit être définie sur 4 (non limité).</span><span class="sxs-lookup"><span data-stu-id="6972a-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="6972a-433">Cette propriété est héritée de la [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6972a-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="6972a-434">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-434">Value</span></span>                                                                        | <span data-ttu-id="6972a-435">Signification</span><span class="sxs-lookup"><span data-stu-id="6972a-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="6972a-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="6972a-437">Non restreint</span><span class="sxs-lookup"><span data-stu-id="6972a-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6972a-438">Notes</span><span class="sxs-lookup"><span data-stu-id="6972a-438">Remarks</span></span>

<span data-ttu-id="6972a-439">L’accès à la classe **MSVM \_ SerialPort** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="6972a-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6972a-440">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6972a-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6972a-441">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6972a-441">Requirements</span></span>



| <span data-ttu-id="6972a-442">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6972a-442">Requirement</span></span> | <span data-ttu-id="6972a-443">Valeur</span><span class="sxs-lookup"><span data-stu-id="6972a-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6972a-444">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6972a-444">Minimum supported client</span></span><br/> | <span data-ttu-id="6972a-445">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6972a-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6972a-446">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6972a-446">Minimum supported server</span></span><br/> | <span data-ttu-id="6972a-447">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6972a-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6972a-448">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6972a-448">Namespace</span></span><br/>                | <span data-ttu-id="6972a-449">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6972a-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6972a-450">MOF</span><span class="sxs-lookup"><span data-stu-id="6972a-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6972a-451"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6972a-452">DLL</span><span class="sxs-lookup"><span data-stu-id="6972a-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6972a-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6972a-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6972a-454">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6972a-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6972a-455">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="6972a-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="6972a-456">[**\_LOGICALPORT CIM**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6972a-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6972a-457">Classes d’appareils série</span><span class="sxs-lookup"><span data-stu-id="6972a-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

