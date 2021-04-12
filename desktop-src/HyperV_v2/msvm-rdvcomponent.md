---
description: Représente l’état du composant RDV, qui est chargé de fournir un transport pour le parent à l’invité à des fins de configuration.
ms.assetid: 240d2659-01ec-4300-a17e-0b1ec90483df
title: Classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent
- Msvm_RdvComponent.RequestStateChange
- Msvm_RdvComponent.SetPowerState
- Msvm_RdvComponent.Reset
- Msvm_RdvComponent.EnableDevice
- Msvm_RdvComponent.OnlineDevice
- Msvm_RdvComponent.QuiesceDevice
- Msvm_RdvComponent.SaveProperties
- Msvm_RdvComponent.RestoreProperties
- Msvm_RdvComponent.InstanceID
- Msvm_RdvComponent.Caption
- Msvm_RdvComponent.Description
- Msvm_RdvComponent.ElementName
- Msvm_RdvComponent.InstallDate
- Msvm_RdvComponent.Name
- Msvm_RdvComponent.OperationalStatus
- Msvm_RdvComponent.StatusDescriptions
- Msvm_RdvComponent.Status
- Msvm_RdvComponent.HealthState
- Msvm_RdvComponent.CommunicationStatus
- Msvm_RdvComponent.DetailedStatus
- Msvm_RdvComponent.OperatingStatus
- Msvm_RdvComponent.PrimaryStatus
- Msvm_RdvComponent.EnabledState
- Msvm_RdvComponent.OtherEnabledState
- Msvm_RdvComponent.RequestedState
- Msvm_RdvComponent.EnabledDefault
- Msvm_RdvComponent.TimeOfLastStateChange
- Msvm_RdvComponent.AvailableRequestedStates
- Msvm_RdvComponent.TransitioningToState
- Msvm_RdvComponent.SystemCreationClassName
- Msvm_RdvComponent.SystemName
- Msvm_RdvComponent.CreationClassName
- Msvm_RdvComponent.DeviceID
- Msvm_RdvComponent.PowerManagementSupported
- Msvm_RdvComponent.PowerManagementCapabilities
- Msvm_RdvComponent.Availability
- Msvm_RdvComponent.StatusInfo
- Msvm_RdvComponent.LastErrorCode
- Msvm_RdvComponent.ErrorDescription
- Msvm_RdvComponent.ErrorCleared
- Msvm_RdvComponent.OtherIdentifyingInfo
- Msvm_RdvComponent.PowerOnHours
- Msvm_RdvComponent.TotalPowerOnHours
- Msvm_RdvComponent.IdentifyingDescriptions
- Msvm_RdvComponent.AdditionalAvailability
- Msvm_RdvComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e1dbffb7db18ef2441d4c8e06cff23af2648e5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203083"
---
# <a name="msvm_rdvcomponent-class"></a><span data-ttu-id="ea8cc-103">MSVM \_ RdvComponent, classe</span><span class="sxs-lookup"><span data-stu-id="ea8cc-103">Msvm\_RdvComponent class</span></span>

<span data-ttu-id="ea8cc-104">Représente l’état du composant RDV, qui est chargé de fournir un transport pour le parent à l’invité à des fins de configuration.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-104">Represents the state of the RDV component, which is responsible for providing a transport for the parent to the guest for configuration purposes.</span></span>

<span data-ttu-id="ea8cc-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8cc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea8cc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "RDV";
  string   Description = "Remote Desktop Virtualization Service";
  string   ElementName = "RDV";
  datetime InstallDate;
  string   Name = "RDV";
  uint16   OperationalStatus[] = {2};
  string   StatusDescriptions[] = {"OK"};
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
  string   CreationClassName = "Msvm_RdvComponent";
  string   DeviceID;
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
};
```

## <a name="members"></a><span data-ttu-id="ea8cc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ea8cc-107">Members</span></span>

<span data-ttu-id="ea8cc-108">La classe **MSVM \_ RdvComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea8cc-108">The **Msvm\_RdvComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="ea8cc-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea8cc-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea8cc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea8cc-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea8cc-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea8cc-111">Methods</span></span>

<span data-ttu-id="ea8cc-112">La classe **MSVM \_ RdvComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-112">The **Msvm\_RdvComponent** class has these methods.</span></span>



| <span data-ttu-id="ea8cc-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea8cc-113">Method</span></span>                                                       | <span data-ttu-id="ea8cc-114">Description</span><span class="sxs-lookup"><span data-stu-id="ea8cc-114">Description</span></span>                                                                                                                                                                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8cc-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="ea8cc-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-116">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="ea8cc-117">**EnableEndPoints**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-117">**EnableEndPoints**</span></span>](enableendpoints-msvm-rdvcomponent.md) | <span data-ttu-id="ea8cc-118">Demande à l’appareil virtuel Services Bureau à distance de démarrer une connexion de canal avec l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-118">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span> <span data-ttu-id="ea8cc-119">Si la valeur zéro (0) est retournée, l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-119">If zero (0) is returned, then the operation was successful.</span></span> <span data-ttu-id="ea8cc-120">Tout autre code de retour indique une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-120">Any other return code indicates an error condition.</span></span><br/> |
| <span data-ttu-id="ea8cc-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-121">**OnlineDevice**</span></span>                                             | <span data-ttu-id="ea8cc-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-122">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ea8cc-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-123">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="ea8cc-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-124">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ea8cc-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-125">**RequestStateChange**</span></span>                                       | <span data-ttu-id="ea8cc-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-126">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ea8cc-127">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-127">**Reset**</span></span>                                                    | <span data-ttu-id="ea8cc-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-128">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ea8cc-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-129">**RestoreProperties**</span></span>                                        | <span data-ttu-id="ea8cc-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-130">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ea8cc-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-131">**SaveProperties**</span></span>                                           | <span data-ttu-id="ea8cc-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-132">This method is not supported.</span></span><br/>                                                                                                                                                                                            |
| <span data-ttu-id="ea8cc-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-133">**SetPowerState**</span></span>                                            | <span data-ttu-id="ea8cc-134">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-134">This method is not supported.</span></span><br/>                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="ea8cc-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ea8cc-135">Properties</span></span>

<span data-ttu-id="ea8cc-136">La classe **MSVM \_ RdvComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-136">The **Msvm\_RdvComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea8cc-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-138">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-140">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="ea8cc-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-142">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-145">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-145">The primary availability and status of the device.</span></span> <span data-ttu-id="ea8cc-146">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ea8cc-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ea8cc-151">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-155">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-155">A short description of the object.</span></span> <span data-ttu-id="ea8cc-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-158">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-160">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ea8cc-161">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea8cc-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ea8cc-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ea8cc-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ea8cc-170">)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea8cc-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-174">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-174">The scoping system's creation class name.</span></span> <span data-ttu-id="ea8cc-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-176">**Description**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-179">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="ea8cc-179">A description of the object.</span></span> <span data-ttu-id="ea8cc-180">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-184">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ea8cc-185">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea8cc-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ea8cc-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ea8cc-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ea8cc-195">)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea8cc-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-199">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="ea8cc-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-204">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-204">A display name for the object.</span></span> <span data-ttu-id="ea8cc-205">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-209">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-209">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="ea8cc-210">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-211">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-211">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-214">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-214">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ea8cc-215">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="ea8cc-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea8cc-216">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="ea8cc-217">Signification</span><span class="sxs-lookup"><span data-stu-id="ea8cc-217">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="ea8cc-218"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-218"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="ea8cc-219">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-219">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="ea8cc-220"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-220"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="ea8cc-221"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-221"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="ea8cc-222">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-222">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="ea8cc-223"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-223"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="ea8cc-224">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-224">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="ea8cc-225"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-225"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="ea8cc-226">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-226">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="ea8cc-227"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-227"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="ea8cc-228">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-228">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="ea8cc-229"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-229"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="ea8cc-230">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-230">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="ea8cc-231"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-231"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="ea8cc-232">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-232">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="ea8cc-233"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-233"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="ea8cc-234">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-234">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="ea8cc-235"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-235"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="ea8cc-236">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-236">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="ea8cc-237">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-237">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="ea8cc-238">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-238">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="ea8cc-239">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-239"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="ea8cc-240">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-240">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="ea8cc-241">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-241">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="ea8cc-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-243">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-245">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="ea8cc-246">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-250">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="ea8cc-251">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-253">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-255">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-255">The current health of the element.</span></span> <span data-ttu-id="ea8cc-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-258">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-260">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="ea8cc-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="ea8cc-261">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-263">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-265">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-265">The date and time when the object was installed.</span></span> <span data-ttu-id="ea8cc-266">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-266">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="ea8cc-267">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-268">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-268">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-271">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-271">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-272">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-272">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ea8cc-273">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-273">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-275">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-277">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="ea8cc-278">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-279">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-279">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-280">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-280">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-282">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-282">This property has been deprecated.</span></span> <span data-ttu-id="ea8cc-283">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-284">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-284">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-287">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-287">The label by which the object is known.</span></span> <span data-ttu-id="ea8cc-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-289">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-289">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-290">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-292">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ea8cc-292">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ea8cc-293">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea8cc-294">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ea8cc-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-296"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-297"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-298"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-299"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-300"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-301"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-302"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-303"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-304"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-305"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-306"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-307"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-308"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-309"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-310"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-311"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-312"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ea8cc-313"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ea8cc-314">)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-314">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea8cc-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-316">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-318">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-318">The current statuses of the object.</span></span> <span data-ttu-id="ea8cc-319">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-322">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-323">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ea8cc-324">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-324">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="ea8cc-325">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-326">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-326">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-327">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-327">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-329">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-329">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ea8cc-330">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-331">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-331">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-332">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-332">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-334">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-334">The power management capabilities of the device.</span></span> <span data-ttu-id="ea8cc-335">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-335">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-336">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-336">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-337">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-337">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-339">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-339">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ea8cc-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-344">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-344">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="ea8cc-345">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-346">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-346">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-347">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-349">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-349">Provides high level status information.</span></span> <span data-ttu-id="ea8cc-350">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-350">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ea8cc-351">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-351">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ea8cc-352">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ea8cc-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-354"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-355"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-356"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ea8cc-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ea8cc-359">)</span><span class="sxs-lookup"><span data-stu-id="ea8cc-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ea8cc-360">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-360">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-361">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-361">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-363">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-363">The last requested or desired state for the element.</span></span> <span data-ttu-id="ea8cc-364">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-364">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-365">**État**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-366">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-368">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-368">The current status of the object.</span></span> <span data-ttu-id="ea8cc-369">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-369">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-370">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-370">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-371">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-371">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-373">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ea8cc-373">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ea8cc-374">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-375">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-375">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-378">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-378">The current state of the logical device.</span></span> <span data-ttu-id="ea8cc-379">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-379">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-380">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-380">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-381">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-383">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-383">The scoping system's creation class name.</span></span> <span data-ttu-id="ea8cc-384">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-385">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-385">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-386">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-388">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-388">The scoping system's name.</span></span> <span data-ttu-id="ea8cc-389">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ea8cc-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-390">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-390">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-391">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-391">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-393">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-393">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ea8cc-394">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-394">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-395">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-395">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-396">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-398">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-398">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ea8cc-399">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cc-400">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-400">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea8cc-401">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea8cc-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea8cc-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ea8cc-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea8cc-403">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-403">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ea8cc-404">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="ea8cc-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea8cc-405">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea8cc-405">Requirements</span></span>



| <span data-ttu-id="ea8cc-406">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea8cc-406">Requirement</span></span> | <span data-ttu-id="ea8cc-407">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea8cc-407">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8cc-408">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea8cc-408">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8cc-409">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea8cc-409">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ea8cc-410">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea8cc-410">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8cc-411">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea8cc-411">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea8cc-412">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ea8cc-412">Namespace</span></span><br/>                | <span data-ttu-id="ea8cc-413">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="ea8cc-413">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ea8cc-414">MOF</span><span class="sxs-lookup"><span data-stu-id="ea8cc-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea8cc-415"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-415"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea8cc-416">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8cc-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea8cc-417"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cc-417"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

