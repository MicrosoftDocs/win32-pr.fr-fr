---
description: Représente un contrôleur SCSI synthétique.
ms.assetid: 4ABAB4C8-F922-4AA3-8FEE-5F5AA969E8B4
title: Classe Msvm_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SCSIProtocolController
- Msvm_SCSIProtocolController.SetPowerState
- Msvm_SCSIProtocolController.EnableDevice
- Msvm_SCSIProtocolController.OnlineDevice
- Msvm_SCSIProtocolController.QuiesceDevice
- Msvm_SCSIProtocolController.SaveProperties
- Msvm_SCSIProtocolController.RestoreProperties
- Msvm_SCSIProtocolController.InstanceID
- Msvm_SCSIProtocolController.Caption
- Msvm_SCSIProtocolController.Description
- Msvm_SCSIProtocolController.ElementName
- Msvm_SCSIProtocolController.InstallDate
- Msvm_SCSIProtocolController.Name
- Msvm_SCSIProtocolController.OperationalStatus
- Msvm_SCSIProtocolController.StatusDescriptions
- Msvm_SCSIProtocolController.Status
- Msvm_SCSIProtocolController.HealthState
- Msvm_SCSIProtocolController.CommunicationStatus
- Msvm_SCSIProtocolController.DetailedStatus
- Msvm_SCSIProtocolController.OperatingStatus
- Msvm_SCSIProtocolController.PrimaryStatus
- Msvm_SCSIProtocolController.EnabledState
- Msvm_SCSIProtocolController.OtherEnabledState
- Msvm_SCSIProtocolController.RequestedState
- Msvm_SCSIProtocolController.EnabledDefault
- Msvm_SCSIProtocolController.TimeOfLastStateChange
- Msvm_SCSIProtocolController.AvailableRequestedStates
- Msvm_SCSIProtocolController.TransitioningToState
- Msvm_SCSIProtocolController.SystemCreationClassName
- Msvm_SCSIProtocolController.SystemName
- Msvm_SCSIProtocolController.CreationClassName
- Msvm_SCSIProtocolController.DeviceID
- Msvm_SCSIProtocolController.PowerManagementSupported
- Msvm_SCSIProtocolController.PowerManagementCapabilities
- Msvm_SCSIProtocolController.Availability
- Msvm_SCSIProtocolController.StatusInfo
- Msvm_SCSIProtocolController.LastErrorCode
- Msvm_SCSIProtocolController.ErrorDescription
- Msvm_SCSIProtocolController.ErrorCleared
- Msvm_SCSIProtocolController.OtherIdentifyingInfo
- Msvm_SCSIProtocolController.PowerOnHours
- Msvm_SCSIProtocolController.TotalPowerOnHours
- Msvm_SCSIProtocolController.IdentifyingDescriptions
- Msvm_SCSIProtocolController.AdditionalAvailability
- Msvm_SCSIProtocolController.MaxQuiesceTime
- Msvm_SCSIProtocolController.MaxUnitsControlled
- Msvm_SCSIProtocolController.NameFormat
- Msvm_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b65390c7cb03f195e9de39aedc3629688717e0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530387"
---
# <a name="msvm_scsiprotocolcontroller-class"></a><span data-ttu-id="37d22-103">MSVM \_ SCSIProtocolController, classe</span><span class="sxs-lookup"><span data-stu-id="37d22-103">Msvm\_SCSIProtocolController class</span></span>

<span data-ttu-id="37d22-104">Représente un contrôleur SCSI synthétique.</span><span class="sxs-lookup"><span data-stu-id="37d22-104">Represents a synthetic SCSI controller.</span></span> <span data-ttu-id="37d22-105">Un contrôleur SCSI synthétique peut prendre en charge jusqu’à 256 lecteurs.</span><span class="sxs-lookup"><span data-stu-id="37d22-105">A synthetic SCSI controller can support up to 256 drives.</span></span>

<span data-ttu-id="37d22-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37d22-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d22-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37d22-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SCSIProtocolController : CIM_SCSIProtocolController
{
  string   InstanceID;
  string   Caption = "SCSI Controller";
  string   Description = "Microsoft Virtual SCSI Controller";
  string   ElementName = "SCSI Controller";
  datetime InstallDate;
  string   Name = "SCSI Controller";
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
  string   CreationClassName = "Msvm_SCSIProtocolController";
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
  uint32   MaxUnitsControlled = 256;
  uint16   NameFormat = 0;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="37d22-108">Membres</span><span class="sxs-lookup"><span data-stu-id="37d22-108">Members</span></span>

<span data-ttu-id="37d22-109">La classe **MSVM \_ SCSIProtocolController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37d22-109">The **Msvm\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="37d22-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="37d22-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="37d22-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37d22-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="37d22-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="37d22-112">Methods</span></span>

<span data-ttu-id="37d22-113">La classe **MSVM \_ SCSIProtocolController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="37d22-113">The **Msvm\_SCSIProtocolController** class has these methods.</span></span>



| <span data-ttu-id="37d22-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="37d22-114">Method</span></span>                                                                       | <span data-ttu-id="37d22-115">Description</span><span class="sxs-lookup"><span data-stu-id="37d22-115">Description</span></span>                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="37d22-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="37d22-116">**EnableDevice**</span></span>                                                             | <span data-ttu-id="37d22-117">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37d22-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="37d22-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="37d22-118">**OnlineDevice**</span></span>                                                             | <span data-ttu-id="37d22-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37d22-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="37d22-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="37d22-120">**QuiesceDevice**</span></span>                                                            | <span data-ttu-id="37d22-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37d22-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="37d22-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="37d22-122">**RequestStateChange**</span></span>](msvm-scsiprotocolcontroller-requeststatechange.md) | <span data-ttu-id="37d22-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="37d22-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="37d22-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="37d22-124">**Reset**</span></span>](msvm-scsiprotocolcontroller-reset.md)                           | <span data-ttu-id="37d22-125">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="37d22-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="37d22-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="37d22-126">**RestoreProperties**</span></span>                                                        | <span data-ttu-id="37d22-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37d22-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="37d22-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="37d22-128">**SaveProperties**</span></span>                                                           | <span data-ttu-id="37d22-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37d22-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="37d22-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="37d22-130">**SetPowerState**</span></span>                                                            | <span data-ttu-id="37d22-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="37d22-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="37d22-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37d22-132">Properties</span></span>

<span data-ttu-id="37d22-133">La classe **MSVM \_ SCSIProtocolController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="37d22-133">The **Msvm\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37d22-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="37d22-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-135">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-137">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="37d22-137">Any additional availability and status of the device.</span></span> <span data-ttu-id="37d22-138">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="37d22-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="37d22-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-139">Value</span></span>                                                                            | <span data-ttu-id="37d22-140">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-140">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="37d22-141"><dt>6,3</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-141"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="37d22-142"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-142"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="37d22-143">Non applicable</span><span class="sxs-lookup"><span data-stu-id="37d22-143">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-144">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="37d22-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-147">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="37d22-147">The primary availability and status of the device.</span></span> <span data-ttu-id="37d22-148">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="37d22-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="37d22-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-149">Value</span></span>                                                                        | <span data-ttu-id="37d22-150">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-150">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="37d22-151"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-151"><dt>6</dt></span></span> </dl> | <span data-ttu-id="37d22-152">Non applicable</span><span class="sxs-lookup"><span data-stu-id="37d22-152">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-153">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="37d22-153">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-154">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-156">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="37d22-156">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="37d22-157">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-157">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="37d22-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-161">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="37d22-161">A short description of the object.</span></span> <span data-ttu-id="37d22-162">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="37d22-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-164">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-166">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="37d22-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="37d22-167">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="37d22-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="37d22-168">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="37d22-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="37d22-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="37d22-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="37d22-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="37d22-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="37d22-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="37d22-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="37d22-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="37d22-176">)</span><span class="sxs-lookup"><span data-stu-id="37d22-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37d22-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37d22-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-180">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="37d22-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="37d22-181">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="37d22-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-182">**Description**</span><span class="sxs-lookup"><span data-stu-id="37d22-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-185">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="37d22-185">A description of the object.</span></span> <span data-ttu-id="37d22-186">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="37d22-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-188">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-190">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="37d22-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="37d22-191">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="37d22-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="37d22-192">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="37d22-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="37d22-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="37d22-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="37d22-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="37d22-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="37d22-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="37d22-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="37d22-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="37d22-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="37d22-201">)</span><span class="sxs-lookup"><span data-stu-id="37d22-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37d22-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="37d22-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-205">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*».</span><span class="sxs-lookup"><span data-stu-id="37d22-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="37d22-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="37d22-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-209">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="37d22-209">A display name for the object.</span></span> <span data-ttu-id="37d22-210">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="37d22-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-214">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="37d22-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="37d22-215">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37d22-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="37d22-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-216">Value</span></span>                                                                        | <span data-ttu-id="37d22-217">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-217">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="37d22-218"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-218"><dt>2</dt></span></span> </dl> | <span data-ttu-id="37d22-219">activé</span><span class="sxs-lookup"><span data-stu-id="37d22-219">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-220">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="37d22-220">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-221">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-222">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-223">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="37d22-223">The enabled and disabled states of an element.</span></span> <span data-ttu-id="37d22-224">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="37d22-224">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="37d22-225">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37d22-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="37d22-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-226">Value</span></span>                                                                        | <span data-ttu-id="37d22-227">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-227">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="37d22-228"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-228"><dt>5</dt></span></span> </dl> | <span data-ttu-id="37d22-229">Non applicable</span><span class="sxs-lookup"><span data-stu-id="37d22-229">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="37d22-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="37d22-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-233">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="37d22-233">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="37d22-234">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-235">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="37d22-235">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-238">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="37d22-238">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="37d22-239">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-239">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-240">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="37d22-240">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-241">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-243">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="37d22-243">The current health of the element.</span></span> <span data-ttu-id="37d22-244">Cela exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="37d22-244">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="37d22-245">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="37d22-245">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="37d22-246">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-247">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="37d22-247">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-248">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="37d22-248">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-250">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="37d22-250">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="37d22-251">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="37d22-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-252">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="37d22-252">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-253">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="37d22-253">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-255">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="37d22-255">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="37d22-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37d22-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37d22-260">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="37d22-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="37d22-261">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="37d22-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="37d22-262">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-263">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="37d22-263">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-264">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37d22-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-266">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="37d22-266">The last error code reported by the logical device.</span></span> <span data-ttu-id="37d22-267">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="37d22-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-269">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37d22-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-271">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="37d22-271">This property has been deprecated.</span></span> <span data-ttu-id="37d22-272">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="37d22-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-273">**MaxUnitsControlled**</span><span class="sxs-lookup"><span data-stu-id="37d22-273">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-274">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37d22-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-276">Nombre maximal d’unités qui peuvent être contrôlées par ou accessibles via ce contrôleur de protocole.</span><span class="sxs-lookup"><span data-stu-id="37d22-276">The maximum number of units that can be controlled by or accessed through this protocol controller.</span></span> <span data-ttu-id="37d22-277">Cette propriété est héritée de la [**\_ ProtocolController CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="37d22-277">This property is inherited from [**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-278">**Nom**</span><span class="sxs-lookup"><span data-stu-id="37d22-278">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-281">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="37d22-281">The label by which the object is known.</span></span> <span data-ttu-id="37d22-282">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-283">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="37d22-283">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-284">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-286">Identifie la manière dont le nom du contrôleur de protocole SCSI est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="37d22-286">Identifies how the name of the SCSI protocol controller is selected.</span></span> <span data-ttu-id="37d22-287">Cette propriété est héritée de la [**\_ SCSIProtocolController CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="37d22-287">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>



| <span data-ttu-id="37d22-288">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-288">Value</span></span>                                                                        | <span data-ttu-id="37d22-289">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-289">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="37d22-290"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-290"><dt>0</dt></span></span> </dl> | <span data-ttu-id="37d22-291">Unknown</span><span class="sxs-lookup"><span data-stu-id="37d22-291">Unknown</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-292">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="37d22-292">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-293">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-293">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-295">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="37d22-295">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="37d22-296">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="37d22-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="37d22-297">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="37d22-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="37d22-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="37d22-299"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="37d22-300"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="37d22-301"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="37d22-302"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="37d22-303"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="37d22-304"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="37d22-305"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="37d22-306"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="37d22-307"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="37d22-308"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="37d22-309"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="37d22-310"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="37d22-311"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="37d22-312"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="37d22-313"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="37d22-314"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="37d22-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="37d22-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="37d22-317">)</span><span class="sxs-lookup"><span data-stu-id="37d22-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37d22-318">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="37d22-318">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-319">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-319">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-321">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="37d22-321">The current status of the object.</span></span> <span data-ttu-id="37d22-322">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="37d22-323">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-323">Value</span></span>                                                                            | <span data-ttu-id="37d22-324">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-324">Meaning</span></span>       |
|----------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="37d22-325"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-325"><dt>{ 2 }</dt></span></span> </dl> |               |
| <dl> <span data-ttu-id="37d22-326"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-326"><dt>2</dt></span></span> </dl>     | <span data-ttu-id="37d22-327">Ok</span><span class="sxs-lookup"><span data-stu-id="37d22-327">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-328">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="37d22-328">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-331">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="37d22-331">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="37d22-332">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="37d22-332">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="37d22-333">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37d22-333">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-334">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="37d22-334">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-335">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="37d22-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-337">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="37d22-337">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="37d22-338">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="37d22-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-339">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="37d22-339">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-342">Chaîne qui décrit la façon dont le contrôleur de protocole est identifié lorsque la valeur de la méthode **NameFormat** est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="37d22-342">A string that describes how the protocol controller is identified when the **NameFormat** is 1 (Other).</span></span> <span data-ttu-id="37d22-343">Cette propriété est héritée de la [**\_ SCSIProtocolController CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span><span class="sxs-lookup"><span data-stu-id="37d22-343">This property is inherited from [**CIM\_SCSIProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="37d22-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-345">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-347">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="37d22-347">The power management capabilities of the device.</span></span> <span data-ttu-id="37d22-348">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="37d22-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-350">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="37d22-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-352">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="37d22-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="37d22-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="37d22-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-355">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37d22-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-357">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="37d22-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="37d22-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="37d22-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-360">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-362">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="37d22-362">Provides high level status information.</span></span> <span data-ttu-id="37d22-363">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="37d22-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="37d22-364">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="37d22-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="37d22-365">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="37d22-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="37d22-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="37d22-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="37d22-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="37d22-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="37d22-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="37d22-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="37d22-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="37d22-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="37d22-372">)</span><span class="sxs-lookup"><span data-stu-id="37d22-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37d22-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="37d22-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-374">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-376">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="37d22-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="37d22-377">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="37d22-377">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="37d22-378">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="37d22-378">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="37d22-379">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37d22-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="37d22-380">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-380">Value</span></span>                                                                         | <span data-ttu-id="37d22-381">Signification</span><span class="sxs-lookup"><span data-stu-id="37d22-381">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="37d22-382"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-382"><dt>12</dt></span></span> </dl> | <span data-ttu-id="37d22-383">Non applicable</span><span class="sxs-lookup"><span data-stu-id="37d22-383">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="37d22-384">**État**</span><span class="sxs-lookup"><span data-stu-id="37d22-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-386">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-387">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="37d22-387">The current status of the object.</span></span> <span data-ttu-id="37d22-388">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-388">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-389">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="37d22-389">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-390">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="37d22-390">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37d22-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-392">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="37d22-392">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="37d22-393">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="37d22-393">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="37d22-394">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="37d22-394">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-395">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-397">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="37d22-397">The current state of the logical device.</span></span> <span data-ttu-id="37d22-398">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37d22-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-402">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="37d22-402">The scoping system's creation class name.</span></span> <span data-ttu-id="37d22-403">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="37d22-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="37d22-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37d22-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-407">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="37d22-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="37d22-408">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="37d22-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-409">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="37d22-409">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-410">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="37d22-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-412">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="37d22-412">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="37d22-413">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="37d22-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="37d22-414">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="37d22-414">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-415">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37d22-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-417">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="37d22-417">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="37d22-418">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-418">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="37d22-419">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="37d22-419">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37d22-420">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37d22-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37d22-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37d22-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37d22-422">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="37d22-422">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="37d22-423">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="37d22-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37d22-424">Notes</span><span class="sxs-lookup"><span data-stu-id="37d22-424">Remarks</span></span>

<span data-ttu-id="37d22-425">L’accès à la classe **MSVM \_ SCSIProtocolController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="37d22-425">Access to the **Msvm\_SCSIProtocolController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="37d22-426">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="37d22-426">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="37d22-427">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37d22-427">Requirements</span></span>



| <span data-ttu-id="37d22-428">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37d22-428">Requirement</span></span> | <span data-ttu-id="37d22-429">Valeur</span><span class="sxs-lookup"><span data-stu-id="37d22-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d22-430">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d22-430">Minimum supported client</span></span><br/> | <span data-ttu-id="37d22-431">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d22-431">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="37d22-432">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37d22-432">Minimum supported server</span></span><br/> | <span data-ttu-id="37d22-433">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37d22-433">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37d22-434">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37d22-434">Namespace</span></span><br/>                | <span data-ttu-id="37d22-435">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="37d22-435">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="37d22-436">MOF</span><span class="sxs-lookup"><span data-stu-id="37d22-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37d22-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37d22-438">DLL</span><span class="sxs-lookup"><span data-stu-id="37d22-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d22-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37d22-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37d22-440">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d22-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d22-441">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="37d22-441">**CIM\_SCSIProtocolController**</span></span>](cim-scsiprotocolcontroller.md)
</dt> <dt>

[<span data-ttu-id="37d22-442">**\_SCSIPROTOCOLCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="37d22-442">**CIM\_SCSIProtocolController**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)
</dt> <dt>

[<span data-ttu-id="37d22-443">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="37d22-443">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

