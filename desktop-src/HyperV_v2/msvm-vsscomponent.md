---
description: Représente l’état du service Service VSS (VSS), qui implémente le demandeur VSS dans le système d’exploitation invité.
ms.assetid: 4DD38929-1E3F-4105-BC1A-B367516F7B6E
title: Classe Msvm_VssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent
- Msvm_VssComponent.SetPowerState
- Msvm_VssComponent.EnableDevice
- Msvm_VssComponent.OnlineDevice
- Msvm_VssComponent.QuiesceDevice
- Msvm_VssComponent.SaveProperties
- Msvm_VssComponent.RestoreProperties
- Msvm_VssComponent.InstanceID
- Msvm_VssComponent.Caption
- Msvm_VssComponent.Description
- Msvm_VssComponent.ElementName
- Msvm_VssComponent.InstallDate
- Msvm_VssComponent.Name
- Msvm_VssComponent.OperationalStatus
- Msvm_VssComponent.StatusDescriptions
- Msvm_VssComponent.Status
- Msvm_VssComponent.HealthState
- Msvm_VssComponent.CommunicationStatus
- Msvm_VssComponent.DetailedStatus
- Msvm_VssComponent.OperatingStatus
- Msvm_VssComponent.PrimaryStatus
- Msvm_VssComponent.EnabledState
- Msvm_VssComponent.OtherEnabledState
- Msvm_VssComponent.RequestedState
- Msvm_VssComponent.EnabledDefault
- Msvm_VssComponent.TimeOfLastStateChange
- Msvm_VssComponent.AvailableRequestedStates
- Msvm_VssComponent.TransitioningToState
- Msvm_VssComponent.SystemCreationClassName
- Msvm_VssComponent.SystemName
- Msvm_VssComponent.CreationClassName
- Msvm_VssComponent.DeviceID
- Msvm_VssComponent.PowerManagementSupported
- Msvm_VssComponent.PowerManagementCapabilities
- Msvm_VssComponent.Availability
- Msvm_VssComponent.StatusInfo
- Msvm_VssComponent.LastErrorCode
- Msvm_VssComponent.ErrorDescription
- Msvm_VssComponent.ErrorCleared
- Msvm_VssComponent.OtherIdentifyingInfo
- Msvm_VssComponent.PowerOnHours
- Msvm_VssComponent.TotalPowerOnHours
- Msvm_VssComponent.IdentifyingDescriptions
- Msvm_VssComponent.AdditionalAvailability
- Msvm_VssComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab4039ce110af9fa023a662c31d1f9962b080e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515410"
---
# <a name="msvm_vsscomponent-class"></a><span data-ttu-id="d2ea7-103">MSVM \_ VssComponent, classe</span><span class="sxs-lookup"><span data-stu-id="d2ea7-103">Msvm\_VssComponent class</span></span>

<span data-ttu-id="d2ea7-104">Représente l’état du service Service VSS (VSS), qui implémente le demandeur VSS dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-104">Represents the state of the Volume Shadow Copy Service (VSS) service, which implements the VSS Requester in the guest operating system.</span></span>

<span data-ttu-id="d2ea7-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ea7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2ea7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "VSS";
  string   Description = "Microsoft VSS Service";
  string   ElementName = "VSS";
  datetime InstallDate;
  string   Name = "VSS";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VssComponent";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="d2ea7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d2ea7-107">Members</span></span>

<span data-ttu-id="d2ea7-108">La classe **MSVM \_ VssComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d2ea7-108">The **Msvm\_VssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d2ea7-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2ea7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2ea7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2ea7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2ea7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d2ea7-111">Methods</span></span>

<span data-ttu-id="d2ea7-112">La classe **MSVM \_ VssComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-112">The **Msvm\_VssComponent** class has these methods.</span></span>



| <span data-ttu-id="d2ea7-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="d2ea7-113">Method</span></span>                                                             | <span data-ttu-id="d2ea7-114">Description</span><span class="sxs-lookup"><span data-stu-id="d2ea7-114">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d2ea7-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-115">**EnableDevice**</span></span>                                                   | <span data-ttu-id="d2ea7-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ea7-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-117">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="d2ea7-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ea7-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-119">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="d2ea7-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d2ea7-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-121">**RequestStateChange**</span></span>](msvm-vsscomponent-requeststatechange.md) | <span data-ttu-id="d2ea7-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d2ea7-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-123">**Reset**</span></span>](msvm-vsscomponent-reset.md)                           | <span data-ttu-id="d2ea7-124">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d2ea7-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-125">**RestoreProperties**</span></span>                                              | <span data-ttu-id="d2ea7-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ea7-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-127">**SaveProperties**</span></span>                                                 | <span data-ttu-id="d2ea7-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d2ea7-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-129">**SetPowerState**</span></span>                                                  | <span data-ttu-id="d2ea7-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2ea7-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2ea7-131">Properties</span></span>

<span data-ttu-id="d2ea7-132">La classe **MSVM \_ VssComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-132">The **Msvm\_VssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2ea7-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-136">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="d2ea7-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-141">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-141">The primary availability and status of the device.</span></span> <span data-ttu-id="d2ea7-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="d2ea7-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-143">Value</span></span>                                                                        | <span data-ttu-id="d2ea7-144">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d2ea7-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="d2ea7-146">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d2ea7-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ea7-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d2ea7-151">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-155">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-155">A short description of the object.</span></span> <span data-ttu-id="d2ea7-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-158">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-160">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d2ea7-161">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ea7-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ea7-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ea7-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ea7-170">)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ea7-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-174">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-174">The scoping system's creation class name.</span></span> <span data-ttu-id="d2ea7-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-176">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-179">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-179">A description of the object.</span></span> <span data-ttu-id="d2ea7-180">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-184">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d2ea7-185">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ea7-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ea7-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ea7-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ea7-195">)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ea7-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-199">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d2ea7-200">Cette propriété est héritée [**de CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*VMGUID* \\ *GUID*», où *VMGUID* est la propriété **Name** de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associée à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-204">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-204">A display name for the object.</span></span> <span data-ttu-id="d2ea7-205">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-209">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 7 (pas de valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>



| <span data-ttu-id="d2ea7-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-210">Value</span></span>                                                                        | <span data-ttu-id="d2ea7-211">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-211">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="d2ea7-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-212"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d2ea7-213">activé</span><span class="sxs-lookup"><span data-stu-id="d2ea7-213">Enabled</span></span><br/>    |
| <dl> <span data-ttu-id="d2ea7-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-214"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d2ea7-215">Désactivé</span><span class="sxs-lookup"><span data-stu-id="d2ea7-215">Disabled</span></span><br/>   |
| <dl> <span data-ttu-id="d2ea7-216"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-216"><dt>7</dt></span></span> </dl> | <span data-ttu-id="d2ea7-217">Pas de valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d2ea7-217">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ea7-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-219">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-221">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d2ea7-222">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-222">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d2ea7-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-223">Value</span></span>                                                                        | <span data-ttu-id="d2ea7-224">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-224">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="d2ea7-225"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-225"><dt>2</dt></span></span> </dl> | <span data-ttu-id="d2ea7-226">activé</span><span class="sxs-lookup"><span data-stu-id="d2ea7-226">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="d2ea7-227"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-227"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d2ea7-228">Désactivé</span><span class="sxs-lookup"><span data-stu-id="d2ea7-228">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ea7-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-230">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-231">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-232">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-232">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="d2ea7-233">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-237">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode**, ainsi que des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-237">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="d2ea7-238">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-240">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-242">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-242">The current health of the element.</span></span> <span data-ttu-id="d2ea7-243">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-243">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d2ea7-244">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d2ea7-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="d2ea7-246">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-246">Value</span></span>                                                                        | <span data-ttu-id="d2ea7-247">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-247">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="d2ea7-248"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-248"><dt>5</dt></span></span> </dl> | <span data-ttu-id="d2ea7-249">Ok</span><span class="sxs-lookup"><span data-stu-id="d2ea7-249">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ea7-250">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-250">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-251">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-251">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-253">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-253">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="d2ea7-254">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-255">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-255">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-256">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-256">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-258">Date et heure auxquelles le service d’intégration a été installé sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-258">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="d2ea7-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-260">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-260">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-263">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-263">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-264">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-264">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d2ea7-265">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-265">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-266">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-266">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-267">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-269">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-269">The last error code reported by the logical device.</span></span> <span data-ttu-id="d2ea7-270">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-271">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-271">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-272">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-272">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-274">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-274">This property has been deprecated.</span></span> <span data-ttu-id="d2ea7-275">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-276">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-279">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-279">The label by which the object is known.</span></span> <span data-ttu-id="d2ea7-280">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-280">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-281">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-281">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-282">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-284">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-284">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d2ea7-285">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ea7-286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ea7-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-288"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-289"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-290"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-291"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-292"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-293"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-294"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-295"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-296"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-297"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-298"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-299"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-300"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-301"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-302"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-303"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-304"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ea7-305"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ea7-306">)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-306">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ea7-307">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-307">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-308">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-310">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-310">The current status of the element.</span></span> <span data-ttu-id="d2ea7-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="d2ea7-312">Les valeurs possibles pour la valeur de la propriété **OperationalStatus** 0 sont les suivantes \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-312">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="d2ea7-313">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-313">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="d2ea7-314">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-314">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2ea7-315"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-315"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="d2ea7-316"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-316"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="d2ea7-317">Le service fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-317">The service is operating normally.</span></span> <span data-ttu-id="d2ea7-318">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-318">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="d2ea7-319"><dt>**Dégradé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-319"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="d2ea7-320">Le service fonctionne normalement, mais le service invité a négocié une version de protocole de communication compatible.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-320">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="d2ea7-321">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-321">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="d2ea7-322"><dt>**Erreur non récupérable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-322"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="d2ea7-323">L’invité ne prend pas en charge une version de protocole compatible.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-323">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="d2ea7-324">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-324">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="d2ea7-325"><dt>**Aucun contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-325"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="d2ea7-326">Le service invité n’est pas installé ou n’a pas encore été contacté.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-326">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="d2ea7-327"><dt>**Communication perdue**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-327"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="d2ea7-328">Le service invité ne répond plus normalement.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-328">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d2ea7-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-332">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-332">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d2ea7-333">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d2ea7-334">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-336">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-338">Données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-338">Additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="d2ea7-339">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-340">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-340">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-341">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-341">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-343">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-343">The power management capabilities of the device.</span></span> <span data-ttu-id="d2ea7-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-346">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-348">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-348">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="d2ea7-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-350">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-350">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-351">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-353">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-353">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="d2ea7-354">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-355">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-355">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-356">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-358">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-358">Provides high level status information.</span></span> <span data-ttu-id="d2ea7-359">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-359">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d2ea7-360">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-360">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d2ea7-361">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d2ea7-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-362"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-363"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-364"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-365"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-366"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d2ea7-367"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d2ea7-368">)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-368">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2ea7-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-370">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-372">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="d2ea7-373">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d2ea7-374">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-374">Value</span></span>                                                                         | <span data-ttu-id="d2ea7-375">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d2ea7-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d2ea7-377">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d2ea7-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2ea7-378">**État**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-381">Chaîne qui spécifie l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-381">A string that specifies the current status of the object.</span></span> <span data-ttu-id="d2ea7-382">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-384">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-386">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d2ea7-387">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-389">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-391">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-391">The current state of the logical device.</span></span> <span data-ttu-id="d2ea7-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-396">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-396">The scoping system's creation class name.</span></span> <span data-ttu-id="d2ea7-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-399">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-401">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-401">The scoping system's name.</span></span> <span data-ttu-id="d2ea7-402">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-404">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-406">Date ou heure de la dernière modification de l' **EnabledState** de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-406">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="d2ea7-407">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-409">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-411">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="d2ea7-412">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ea7-414">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2ea7-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ea7-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ea7-416">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d2ea7-417">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d2ea7-418">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-418">Value</span></span>                                                                         | <span data-ttu-id="d2ea7-419">Signification</span><span class="sxs-lookup"><span data-stu-id="d2ea7-419">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="d2ea7-420"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-420"><dt>12</dt></span></span> </dl> | <span data-ttu-id="d2ea7-421">Non applicable</span><span class="sxs-lookup"><span data-stu-id="d2ea7-421">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2ea7-422">Notes</span><span class="sxs-lookup"><span data-stu-id="d2ea7-422">Remarks</span></span>

<span data-ttu-id="d2ea7-423">L’accès à la classe **MSVM \_ VssComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-423">Access to the **Msvm\_VssComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d2ea7-424">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ea7-425">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2ea7-425">Requirements</span></span>



| <span data-ttu-id="d2ea7-426">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2ea7-426">Requirement</span></span> | <span data-ttu-id="d2ea7-427">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ea7-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ea7-428">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ea7-428">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ea7-429">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2ea7-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2ea7-430">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ea7-430">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ea7-431">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2ea7-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2ea7-432">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d2ea7-432">Namespace</span></span><br/>                | <span data-ttu-id="d2ea7-433">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2ea7-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2ea7-434">MOF</span><span class="sxs-lookup"><span data-stu-id="d2ea7-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2ea7-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2ea7-436">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ea7-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ea7-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2ea7-438">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2ea7-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ea7-439">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-439">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="d2ea7-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-440">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

