---
description: Représente le contrôleur de disquette sur l’ordinateur virtuel.
ms.assetid: 38A19BF3-0E8F-4DCE-B2DB-B2E3F8100E00
title: Classe Msvm_DisketteController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteController
- Msvm_DisketteController.SetPowerState
- Msvm_DisketteController.EnableDevice
- Msvm_DisketteController.OnlineDevice
- Msvm_DisketteController.QuiesceDevice
- Msvm_DisketteController.SaveProperties
- Msvm_DisketteController.RestoreProperties
- Msvm_DisketteController.InstanceID
- Msvm_DisketteController.Caption
- Msvm_DisketteController.Description
- Msvm_DisketteController.ElementName
- Msvm_DisketteController.InstallDate
- Msvm_DisketteController.Name
- Msvm_DisketteController.OperationalStatus
- Msvm_DisketteController.StatusDescriptions
- Msvm_DisketteController.Status
- Msvm_DisketteController.HealthState
- Msvm_DisketteController.CommunicationStatus
- Msvm_DisketteController.DetailedStatus
- Msvm_DisketteController.OperatingStatus
- Msvm_DisketteController.PrimaryStatus
- Msvm_DisketteController.EnabledState
- Msvm_DisketteController.OtherEnabledState
- Msvm_DisketteController.RequestedState
- Msvm_DisketteController.EnabledDefault
- Msvm_DisketteController.TimeOfLastStateChange
- Msvm_DisketteController.AvailableRequestedStates
- Msvm_DisketteController.TransitioningToState
- Msvm_DisketteController.SystemCreationClassName
- Msvm_DisketteController.SystemName
- Msvm_DisketteController.CreationClassName
- Msvm_DisketteController.DeviceID
- Msvm_DisketteController.PowerManagementSupported
- Msvm_DisketteController.PowerManagementCapabilities
- Msvm_DisketteController.Availability
- Msvm_DisketteController.StatusInfo
- Msvm_DisketteController.LastErrorCode
- Msvm_DisketteController.ErrorDescription
- Msvm_DisketteController.ErrorCleared
- Msvm_DisketteController.OtherIdentifyingInfo
- Msvm_DisketteController.PowerOnHours
- Msvm_DisketteController.TotalPowerOnHours
- Msvm_DisketteController.IdentifyingDescriptions
- Msvm_DisketteController.AdditionalAvailability
- Msvm_DisketteController.MaxQuiesceTime
- Msvm_DisketteController.TimeOfLastReset
- Msvm_DisketteController.ProtocolSupported
- Msvm_DisketteController.MaxNumberControlled
- Msvm_DisketteController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f1e4e731464e25dc8e871ebd17cdcddd4e262673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751173"
---
# <a name="msvm_diskettecontroller-class"></a><span data-ttu-id="67ffd-103">MSVM \_ DisketteController, classe</span><span class="sxs-lookup"><span data-stu-id="67ffd-103">Msvm\_DisketteController class</span></span>

<span data-ttu-id="67ffd-104">Représente le contrôleur de disquette sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="67ffd-104">Represents the floppy controller in the virtual machine.</span></span> <span data-ttu-id="67ffd-105">Le contrôleur de disquette est fixe ; par conséquent, aucun pool de ressources ne lui est associé.</span><span class="sxs-lookup"><span data-stu-id="67ffd-105">The floppy controller is fixed, therefore there is no resource pool associated with it.</span></span>

<span data-ttu-id="67ffd-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="67ffd-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ffd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67ffd-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteController : CIM_Controller
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName = "Msvm_DisketteController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 7;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Diskette Protocol";
};
```

## <a name="members"></a><span data-ttu-id="67ffd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="67ffd-108">Members</span></span>

<span data-ttu-id="67ffd-109">La classe **MSVM \_ DisketteController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67ffd-109">The **Msvm\_DisketteController** class has these types of members:</span></span>

-   [<span data-ttu-id="67ffd-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67ffd-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="67ffd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67ffd-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="67ffd-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67ffd-112">Methods</span></span>

<span data-ttu-id="67ffd-113">La classe **MSVM \_ DisketteController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="67ffd-113">The **Msvm\_DisketteController** class has these methods.</span></span>



| <span data-ttu-id="67ffd-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="67ffd-114">Method</span></span>                                                                   | <span data-ttu-id="67ffd-115">Description</span><span class="sxs-lookup"><span data-stu-id="67ffd-115">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="67ffd-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="67ffd-116">**EnableDevice**</span></span>                                                         | <span data-ttu-id="67ffd-117">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67ffd-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="67ffd-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="67ffd-118">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="67ffd-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67ffd-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="67ffd-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="67ffd-120">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="67ffd-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67ffd-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="67ffd-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="67ffd-122">**RequestStateChange**</span></span>](msvm-diskettecontroller-requeststatechange.md) | <span data-ttu-id="67ffd-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="67ffd-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="67ffd-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="67ffd-124">**Reset**</span></span>](msvm-diskettecontroller-reset.md)                           | <span data-ttu-id="67ffd-125">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="67ffd-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="67ffd-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="67ffd-126">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="67ffd-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67ffd-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="67ffd-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="67ffd-128">**SaveProperties**</span></span>                                                       | <span data-ttu-id="67ffd-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67ffd-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="67ffd-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="67ffd-130">**SetPowerState**</span></span>                                                        | <span data-ttu-id="67ffd-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="67ffd-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="67ffd-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67ffd-132">Properties</span></span>

<span data-ttu-id="67ffd-133">La classe **MSVM \_ DisketteController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="67ffd-133">The **Msvm\_DisketteController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67ffd-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="67ffd-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-135">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="67ffd-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="67ffd-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="67ffd-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-142">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="67ffd-142">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-143">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-143">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-145">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="67ffd-145">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="67ffd-146">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffd-146">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="67ffd-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-150">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67ffd-150">A short description of the object.</span></span> <span data-ttu-id="67ffd-151">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-152">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="67ffd-152">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-155">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="67ffd-155">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="67ffd-156">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="67ffd-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="67ffd-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="67ffd-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="67ffd-159"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="67ffd-160"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="67ffd-161"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="67ffd-162"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="67ffd-163"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="67ffd-164"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="67ffd-165">)</span><span class="sxs-lookup"><span data-stu-id="67ffd-165">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67ffd-166">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67ffd-166">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-169">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="67ffd-169">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="67ffd-170">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « MSVM \_ DisketteController ».</span><span class="sxs-lookup"><span data-stu-id="67ffd-170">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_DisketteController".</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-171">**Description**</span><span class="sxs-lookup"><span data-stu-id="67ffd-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-174">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="67ffd-174">A description of the object.</span></span> <span data-ttu-id="67ffd-175">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="67ffd-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-177">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-179">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="67ffd-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="67ffd-180">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="67ffd-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="67ffd-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="67ffd-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="67ffd-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="67ffd-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="67ffd-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="67ffd-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="67ffd-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="67ffd-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="67ffd-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="67ffd-190">)</span><span class="sxs-lookup"><span data-stu-id="67ffd-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67ffd-191">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="67ffd-191">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-194">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="67ffd-194">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="67ffd-195">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="67ffd-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-196">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="67ffd-196">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-199">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67ffd-199">A display name for the object.</span></span> <span data-ttu-id="67ffd-200">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-201">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="67ffd-201">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-204">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="67ffd-204">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="67ffd-205">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffd-205">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="67ffd-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-209">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="67ffd-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="67ffd-210">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="67ffd-210">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="67ffd-211">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffd-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="67ffd-212">Valeur</span><span class="sxs-lookup"><span data-stu-id="67ffd-212">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="67ffd-213">Signification</span><span class="sxs-lookup"><span data-stu-id="67ffd-213">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="67ffd-214"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="67ffd-215">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="67ffd-215">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="67ffd-216"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-216"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="67ffd-217"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-217"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="67ffd-218">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="67ffd-218">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="67ffd-219"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-219"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="67ffd-220">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="67ffd-220">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="67ffd-221"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-221"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="67ffd-222">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="67ffd-222">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="67ffd-223"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-223"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="67ffd-224">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="67ffd-224">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="67ffd-225"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-225"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="67ffd-226">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="67ffd-226">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="67ffd-227"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-227"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="67ffd-228">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="67ffd-228">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="67ffd-229"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-229"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="67ffd-230">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="67ffd-230">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="67ffd-231"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-231"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="67ffd-232">L’élément est activé, mais il est en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="67ffd-232">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="67ffd-233">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="67ffd-233">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="67ffd-234">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="67ffd-234">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="67ffd-235">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-235"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="67ffd-236">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="67ffd-236">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="67ffd-237">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="67ffd-237">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="67ffd-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="67ffd-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-239">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="67ffd-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-241">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-241">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-242">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="67ffd-242">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-245">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-246">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="67ffd-246">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-247">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-249">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="67ffd-249">The current health of the element.</span></span> <span data-ttu-id="67ffd-250">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="67ffd-250">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="67ffd-251">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="67ffd-251">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="67ffd-252">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-253">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="67ffd-253">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-254">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="67ffd-254">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-256">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="67ffd-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-257">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="67ffd-257">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-258">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67ffd-258">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-260">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="67ffd-260">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="67ffd-261">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-262">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="67ffd-262">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-265">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="67ffd-265">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-266">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="67ffd-266">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="67ffd-267">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-267">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-268">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="67ffd-268">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-269">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffd-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-271">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-272">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="67ffd-272">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-273">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67ffd-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-275">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="67ffd-275">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="67ffd-276">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="67ffd-276">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="67ffd-277">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="67ffd-277">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="67ffd-278">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)et est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="67ffd-278">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="67ffd-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-280">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffd-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-282">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-283">**Nom**</span><span class="sxs-lookup"><span data-stu-id="67ffd-283">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-284">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-286">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="67ffd-286">The label by which the object is known.</span></span> <span data-ttu-id="67ffd-287">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-288">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="67ffd-288">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-289">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-290">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-291">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="67ffd-291">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="67ffd-292">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-292">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="67ffd-293">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="67ffd-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="67ffd-294"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="67ffd-295"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="67ffd-296"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="67ffd-297"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="67ffd-298"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="67ffd-299"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="67ffd-300"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="67ffd-301"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="67ffd-302"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="67ffd-303"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="67ffd-304"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="67ffd-305"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="67ffd-306"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="67ffd-307"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="67ffd-308"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="67ffd-309"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="67ffd-310"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="67ffd-311"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="67ffd-312"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="67ffd-313">)</span><span class="sxs-lookup"><span data-stu-id="67ffd-313">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67ffd-314">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="67ffd-314">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-315">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-315">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-317">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67ffd-317">The current statuses of the object.</span></span> <span data-ttu-id="67ffd-318">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-319">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="67ffd-319">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-320">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-322">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="67ffd-322">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="67ffd-323">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="67ffd-323">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="67ffd-324">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="67ffd-324">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-325">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="67ffd-325">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-326">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="67ffd-326">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-327">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-328">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="67ffd-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-329">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="67ffd-329">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-330">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-330">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-332">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-332">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-333">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="67ffd-333">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-334">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="67ffd-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-336">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-337">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="67ffd-337">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-338">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffd-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-341">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="67ffd-341">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-342">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-342">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-344">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="67ffd-344">Provides high level status information.</span></span> <span data-ttu-id="67ffd-345">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="67ffd-345">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="67ffd-346">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-346">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="67ffd-347">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="67ffd-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="67ffd-348"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="67ffd-349"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="67ffd-350"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="67ffd-351"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="67ffd-352"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="67ffd-353"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="67ffd-354">)</span><span class="sxs-lookup"><span data-stu-id="67ffd-354">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67ffd-355">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="67ffd-355">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-356">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-358">Chaîne qui fournit des informations supplémentaires relatives au protocole pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="67ffd-358">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="67ffd-359">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)et est définie sur « protocole de disquette ».</span><span class="sxs-lookup"><span data-stu-id="67ffd-359">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to "Diskette Protocol".</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-360">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="67ffd-360">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-361">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-363">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="67ffd-363">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="67ffd-364">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)et est définie sur 7 (disquette flexible).</span><span class="sxs-lookup"><span data-stu-id="67ffd-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is set to 7 (Flexible Diskette).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-365">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="67ffd-365">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-366">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-368">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="67ffd-368">The last requested or desired state for the element.</span></span> <span data-ttu-id="67ffd-369">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="67ffd-369">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="67ffd-370">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="67ffd-370">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="67ffd-371">Une instance particulière d’un élément logique activé ne prend peut-être pas en charge **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="67ffd-371">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="67ffd-372">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-372">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="67ffd-373">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffd-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-374">**État**</span><span class="sxs-lookup"><span data-stu-id="67ffd-374">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-375">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-377">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="67ffd-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-379">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="67ffd-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-381">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="67ffd-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="67ffd-382">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="67ffd-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="67ffd-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-384">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-386">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-387">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67ffd-387">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-390">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="67ffd-390">The scoping system's creation class name.</span></span> <span data-ttu-id="67ffd-391">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="67ffd-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-392">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="67ffd-392">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-393">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67ffd-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-395">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="67ffd-395">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="67ffd-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="67ffd-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-397">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="67ffd-397">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-398">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67ffd-398">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-400">La dernière fois que la machine virtuelle a été mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="67ffd-400">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="67ffd-401">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="67ffd-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-402">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="67ffd-402">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-403">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67ffd-403">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-405">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="67ffd-405">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="67ffd-406">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="67ffd-406">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-407">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="67ffd-407">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-408">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67ffd-408">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-410">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="67ffd-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67ffd-411">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="67ffd-411">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67ffd-412">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67ffd-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67ffd-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67ffd-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67ffd-414">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="67ffd-414">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="67ffd-415">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="67ffd-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67ffd-416">Notes</span><span class="sxs-lookup"><span data-stu-id="67ffd-416">Remarks</span></span>

<span data-ttu-id="67ffd-417">L’accès à la classe **MSVM \_ DisketteController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="67ffd-417">Access to the **Msvm\_DisketteController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67ffd-418">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="67ffd-418">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ffd-419">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67ffd-419">Requirements</span></span>



| <span data-ttu-id="67ffd-420">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67ffd-420">Requirement</span></span> | <span data-ttu-id="67ffd-421">Valeur</span><span class="sxs-lookup"><span data-stu-id="67ffd-421">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ffd-422">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67ffd-422">Minimum supported client</span></span><br/> | <span data-ttu-id="67ffd-423">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67ffd-423">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67ffd-424">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67ffd-424">Minimum supported server</span></span><br/> | <span data-ttu-id="67ffd-425">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67ffd-425">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67ffd-426">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="67ffd-426">Namespace</span></span><br/>                | <span data-ttu-id="67ffd-427">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="67ffd-427">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67ffd-428">MOF</span><span class="sxs-lookup"><span data-stu-id="67ffd-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67ffd-429"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-429"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67ffd-430">DLL</span><span class="sxs-lookup"><span data-stu-id="67ffd-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ffd-431"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67ffd-431"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67ffd-432">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67ffd-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ffd-433">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="67ffd-433">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="67ffd-434">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="67ffd-434">**CIM\_Controller**</span></span>](/windows/desktop/CIMWin32Prov/cim-controller)
</dt> <dt>

[<span data-ttu-id="67ffd-435">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="67ffd-435">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

