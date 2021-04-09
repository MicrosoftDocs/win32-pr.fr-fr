---
description: Représente l’état du service d’échange de paires clé/valeur, qui fournit un mécanisme permettant d’échanger des données entre l’ordinateur virtuel et le système d’exploitation s’exécutant sur le système d’exploitation de gestion.
ms.assetid: AA68BC74-A919-4029-B703-E08F00449F20
title: Classe Msvm_KvpExchangeComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponent
- Msvm_KvpExchangeComponent.SetPowerState
- Msvm_KvpExchangeComponent.EnableDevice
- Msvm_KvpExchangeComponent.OnlineDevice
- Msvm_KvpExchangeComponent.QuiesceDevice
- Msvm_KvpExchangeComponent.SaveProperties
- Msvm_KvpExchangeComponent.RestoreProperties
- Msvm_KvpExchangeComponent.InstanceID
- Msvm_KvpExchangeComponent.Caption
- Msvm_KvpExchangeComponent.Description
- Msvm_KvpExchangeComponent.ElementName
- Msvm_KvpExchangeComponent.InstallDate
- Msvm_KvpExchangeComponent.Name
- Msvm_KvpExchangeComponent.OperationalStatus
- Msvm_KvpExchangeComponent.StatusDescriptions
- Msvm_KvpExchangeComponent.Status
- Msvm_KvpExchangeComponent.HealthState
- Msvm_KvpExchangeComponent.CommunicationStatus
- Msvm_KvpExchangeComponent.DetailedStatus
- Msvm_KvpExchangeComponent.OperatingStatus
- Msvm_KvpExchangeComponent.PrimaryStatus
- Msvm_KvpExchangeComponent.EnabledState
- Msvm_KvpExchangeComponent.OtherEnabledState
- Msvm_KvpExchangeComponent.RequestedState
- Msvm_KvpExchangeComponent.EnabledDefault
- Msvm_KvpExchangeComponent.TimeOfLastStateChange
- Msvm_KvpExchangeComponent.AvailableRequestedStates
- Msvm_KvpExchangeComponent.TransitioningToState
- Msvm_KvpExchangeComponent.SystemCreationClassName
- Msvm_KvpExchangeComponent.SystemName
- Msvm_KvpExchangeComponent.CreationClassName
- Msvm_KvpExchangeComponent.DeviceID
- Msvm_KvpExchangeComponent.PowerManagementSupported
- Msvm_KvpExchangeComponent.PowerManagementCapabilities
- Msvm_KvpExchangeComponent.Availability
- Msvm_KvpExchangeComponent.StatusInfo
- Msvm_KvpExchangeComponent.LastErrorCode
- Msvm_KvpExchangeComponent.ErrorDescription
- Msvm_KvpExchangeComponent.ErrorCleared
- Msvm_KvpExchangeComponent.OtherIdentifyingInfo
- Msvm_KvpExchangeComponent.PowerOnHours
- Msvm_KvpExchangeComponent.TotalPowerOnHours
- Msvm_KvpExchangeComponent.IdentifyingDescriptions
- Msvm_KvpExchangeComponent.AdditionalAvailability
- Msvm_KvpExchangeComponent.MaxQuiesceTime
- Msvm_KvpExchangeComponent.GuestExchangeItems
- Msvm_KvpExchangeComponent.GuestIntrinsicExchangeItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3aa7f269d24c284eef3ad2c519f5fdbf48513a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868513"
---
# <a name="msvm_kvpexchangecomponent-class"></a><span data-ttu-id="18358-103">MSVM \_ KvpExchangeComponent, classe</span><span class="sxs-lookup"><span data-stu-id="18358-103">Msvm\_KvpExchangeComponent class</span></span>

<span data-ttu-id="18358-104">Représente l’état du service d’échange de paires clé/valeur, qui fournit un mécanisme permettant d’échanger des données entre l’ordinateur virtuel et le système d’exploitation s’exécutant sur le système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="18358-104">Represents the state of the key/value pair exchange service, which provides a mechanism to exchange data between the virtual machine and the operating system running on the management operating system.</span></span>

<span data-ttu-id="18358-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="18358-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18358-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18358-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Key-Value Pair Exchange";
  string   Description = "Microsoft Key-Value Pair Exchange Service";
  string   ElementName = "Key-Value pair Exchange";
  datetime InstallDate;
  string   Name = "Key-Value Pair Exchange";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_KvpExchangeComponent";
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
  string   GuestExchangeItems[];
  string   GuestIntrinsicExchangeItems[];
};
```

## <a name="members"></a><span data-ttu-id="18358-107">Membres</span><span class="sxs-lookup"><span data-stu-id="18358-107">Members</span></span>

<span data-ttu-id="18358-108">La classe **MSVM \_ KvpExchangeComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18358-108">The **Msvm\_KvpExchangeComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="18358-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18358-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="18358-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18358-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18358-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18358-111">Methods</span></span>

<span data-ttu-id="18358-112">La classe **MSVM \_ KvpExchangeComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="18358-112">The **Msvm\_KvpExchangeComponent** class has these methods.</span></span>



| <span data-ttu-id="18358-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="18358-113">Method</span></span>                                                                     | <span data-ttu-id="18358-114">Description</span><span class="sxs-lookup"><span data-stu-id="18358-114">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="18358-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="18358-115">**EnableDevice**</span></span>                                                           | <span data-ttu-id="18358-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18358-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18358-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="18358-117">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="18358-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18358-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18358-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="18358-119">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="18358-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18358-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="18358-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="18358-121">**RequestStateChange**</span></span>](msvm-kvpexchangecomponent-requeststatechange.md) | <span data-ttu-id="18358-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="18358-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="18358-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="18358-123">**Reset**</span></span>](msvm-kvpexchangecomponent-reset.md)                           | <span data-ttu-id="18358-124">Réinitialise le composant.</span><span class="sxs-lookup"><span data-stu-id="18358-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="18358-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="18358-125">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="18358-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18358-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18358-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="18358-127">**SaveProperties**</span></span>                                                         | <span data-ttu-id="18358-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18358-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18358-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18358-129">**SetPowerState**</span></span>                                                          | <span data-ttu-id="18358-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18358-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="18358-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18358-131">Properties</span></span>

<span data-ttu-id="18358-132">La classe **MSVM \_ KvpExchangeComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="18358-132">The **Msvm\_KvpExchangeComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18358-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="18358-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-136">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18358-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="18358-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="18358-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="18358-138">Value</span></span>                                                                            | <span data-ttu-id="18358-139">Signification</span><span class="sxs-lookup"><span data-stu-id="18358-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18358-140"><dt>6,3</dt></span><span class="sxs-lookup"><span data-stu-id="18358-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="18358-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="18358-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="18358-142">Non applicable</span><span class="sxs-lookup"><span data-stu-id="18358-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18358-143">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="18358-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-146">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18358-146">The primary availability and status of the device.</span></span> <span data-ttu-id="18358-147">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="18358-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="18358-148">Value</span></span>                                                                        | <span data-ttu-id="18358-149">Signification</span><span class="sxs-lookup"><span data-stu-id="18358-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18358-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="18358-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="18358-151">Non applicable</span><span class="sxs-lookup"><span data-stu-id="18358-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18358-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="18358-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-153">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-155">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="18358-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="18358-156">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18358-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-160">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18358-160">A short description of the object.</span></span> <span data-ttu-id="18358-161">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18358-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="18358-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-163">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-165">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="18358-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="18358-166">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18358-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18358-167">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18358-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18358-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18358-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="18358-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18358-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="18358-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18358-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="18358-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18358-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="18358-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18358-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18358-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18358-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18358-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18358-175">)</span><span class="sxs-lookup"><span data-stu-id="18358-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18358-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18358-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-179">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18358-179">The scoping system's creation class name.</span></span> <span data-ttu-id="18358-180">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18358-181">**Description**</span><span class="sxs-lookup"><span data-stu-id="18358-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-184">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="18358-184">A description of the object.</span></span> <span data-ttu-id="18358-185">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18358-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="18358-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-187">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-189">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="18358-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="18358-190">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18358-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18358-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18358-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="18358-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18358-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="18358-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18358-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="18358-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18358-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="18358-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18358-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="18358-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18358-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="18358-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18358-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18358-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18358-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18358-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18358-200">)</span><span class="sxs-lookup"><span data-stu-id="18358-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18358-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="18358-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-204">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18358-204">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="18358-205">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18358-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="18358-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-209">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18358-209">A display name for the object.</span></span> <span data-ttu-id="18358-210">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18358-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="18358-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-214">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18358-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18358-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="18358-215">Value</span></span>                                                                        | <span data-ttu-id="18358-216">Signification</span><span class="sxs-lookup"><span data-stu-id="18358-216">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="18358-217"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="18358-217"><dt>7</dt></span></span> </dl> | <span data-ttu-id="18358-218">Pas de valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="18358-218">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18358-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="18358-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-220">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-222">État activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18358-222">The enabled state of the element.</span></span> <span data-ttu-id="18358-223">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18358-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="18358-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="18358-224"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18358-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="18358-225"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18358-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18358-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-227">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18358-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18358-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-229">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="18358-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="18358-230">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18358-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-234">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="18358-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="18358-235">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-236">**GuestExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="18358-236">**GuestExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-237">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18358-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18358-239">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="18358-239">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="18358-240">Tableau d’instances [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incorporées qui contiennent l’ensemble de paires clé-valeur que les services en cours d’exécution dans le système d’exploitation invité ont poussés pour pouvoir accéder aux clients externes.</span><span class="sxs-lookup"><span data-stu-id="18358-240">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that services running within the guest operating system have pushed up to be available for access by external clients.</span></span> <span data-ttu-id="18358-241">Ce tableau ne contient pas d’éléments intrinsèques qui sont envoyés directement par le service d’intégration.</span><span class="sxs-lookup"><span data-stu-id="18358-241">This array will not contain any intrinsic items that are pushed by the integration service directly.</span></span>

</dd> <dt>

<span data-ttu-id="18358-242">**GuestIntrinsicExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="18358-242">**GuestIntrinsicExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-243">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18358-243">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18358-245">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="18358-245">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="18358-246">Tableau d’instances [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incorporées qui contiennent l’ensemble de paires clé-valeur que le système d’exploitation invité a envoyées pour pouvoir être accessibles aux clients externes.</span><span class="sxs-lookup"><span data-stu-id="18358-246">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances which contain the set of key-value pairs that the guest operating system has pushed up to be available for access by external clients.</span></span> <span data-ttu-id="18358-247">Ce tableau ne contient pas d’éléments de données envoyés par d’autres services exécutés dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="18358-247">This array will not contain any data items pushed by other services running within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="18358-248">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="18358-248">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-249">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-249">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-251">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18358-251">The current health of the element.</span></span> <span data-ttu-id="18358-252">Cela exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="18358-252">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="18358-253">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="18358-253">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="18358-254">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-255">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18358-255">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-256">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18358-256">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-258">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="18358-258">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="18358-259">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-259">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-260">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18358-260">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-261">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18358-261">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18358-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-263">Date et heure auxquelles le service d’intégration a été installé sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="18358-263">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="18358-264">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-264">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-265">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18358-265">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-266">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18358-268">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="18358-268">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18358-269">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="18358-269">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="18358-270">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18358-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-271">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18358-271">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-272">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18358-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18358-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-274">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18358-274">The last error code reported by the logical device.</span></span> <span data-ttu-id="18358-275">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-275">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="18358-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-277">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18358-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18358-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-279">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="18358-279">This property has been deprecated.</span></span> <span data-ttu-id="18358-280">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18358-281">**Nom**</span><span class="sxs-lookup"><span data-stu-id="18358-281">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-284">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="18358-284">The label by which the object is known.</span></span> <span data-ttu-id="18358-285">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-286">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="18358-286">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-287">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-289">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="18358-289">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="18358-290">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18358-290">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18358-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18358-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18358-292"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18358-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="18358-293"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18358-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="18358-294"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18358-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="18358-295"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18358-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="18358-296"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18358-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="18358-297"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18358-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="18358-298"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="18358-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="18358-299"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="18358-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="18358-300"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="18358-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="18358-301"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="18358-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="18358-302"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="18358-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="18358-303"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="18358-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="18358-304"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="18358-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="18358-305"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="18358-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="18358-306"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="18358-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="18358-307"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="18358-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="18358-308"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="18358-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18358-309"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18358-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18358-310"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18358-311">)</span><span class="sxs-lookup"><span data-stu-id="18358-311">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18358-312">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="18358-312">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-313">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-315">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18358-315">The current status of the element.</span></span> <span data-ttu-id="18358-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="18358-317">Les valeurs possibles pour la valeur de la propriété **OperationalStatus** 0 sont les suivantes \[ \] .</span><span class="sxs-lookup"><span data-stu-id="18358-317">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="18358-318">Valeur</span><span class="sxs-lookup"><span data-stu-id="18358-318">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="18358-319">Signification</span><span class="sxs-lookup"><span data-stu-id="18358-319">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="18358-320"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="18358-320"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="18358-321">Le service fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="18358-321">The service is operating normally.</span></span> <span data-ttu-id="18358-322">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18358-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="18358-323"><dt>**Dégradé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="18358-323"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="18358-324">Le service fonctionne normalement, mais le service invité a négocié une version de protocole de communication compatible.</span><span class="sxs-lookup"><span data-stu-id="18358-324">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="18358-325">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18358-325">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="18358-326"><dt>**Erreur non récupérable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="18358-326"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="18358-327">L’invité ne prend pas en charge une version de protocole compatible.</span><span class="sxs-lookup"><span data-stu-id="18358-327">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="18358-328">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18358-328">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="18358-329"><dt>**Aucun contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="18358-329"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="18358-330">Le service invité n’est pas installé ou n’a pas encore été contacté.</span><span class="sxs-lookup"><span data-stu-id="18358-330">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="18358-331"><dt>**Communication perdue**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="18358-331"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="18358-332">Le service invité ne répond plus normalement.</span><span class="sxs-lookup"><span data-stu-id="18358-332">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="18358-333">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="18358-333">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-336">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="18358-336">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="18358-337">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="18358-337">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="18358-338">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18358-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="18358-339">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="18358-339">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-340">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18358-340">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-342">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="18358-342">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="18358-343">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et prend toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="18358-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18358-344">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18358-344">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-345">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-347">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18358-347">The power management capabilities of the device.</span></span> <span data-ttu-id="18358-348">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-349">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18358-349">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-350">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18358-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18358-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-352">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="18358-352">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="18358-353">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-354">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="18358-354">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-355">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18358-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18358-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-357">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="18358-357">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="18358-358">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-359">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="18358-359">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-360">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-362">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="18358-362">Provides high level status information.</span></span> <span data-ttu-id="18358-363">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="18358-363">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="18358-364">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18358-364">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18358-365">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-365">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18358-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18358-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18358-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="18358-367"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18358-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="18358-368"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18358-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="18358-369"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18358-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18358-370"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18358-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18358-371"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18358-372">)</span><span class="sxs-lookup"><span data-stu-id="18358-372">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18358-373">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="18358-373">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-374">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-376">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="18358-376">The last requested or desired state for the element.</span></span> <span data-ttu-id="18358-377">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18358-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18358-378">Valeur</span><span class="sxs-lookup"><span data-stu-id="18358-378">Value</span></span>                                                                         | <span data-ttu-id="18358-379">Signification</span><span class="sxs-lookup"><span data-stu-id="18358-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18358-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="18358-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="18358-381">Non applicable</span><span class="sxs-lookup"><span data-stu-id="18358-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18358-382">**État**</span><span class="sxs-lookup"><span data-stu-id="18358-382">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-383">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-385">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18358-385">The current status of the object.</span></span> <span data-ttu-id="18358-386">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-387">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18358-387">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-388">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18358-388">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18358-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-390">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="18358-390">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="18358-391">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18358-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18358-392">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18358-392">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-393">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-395">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18358-395">The current state of the logical device.</span></span> <span data-ttu-id="18358-396">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-397">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18358-397">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-398">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-400">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18358-400">The scoping system's creation class name.</span></span> <span data-ttu-id="18358-401">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18358-402">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18358-402">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18358-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18358-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-405">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18358-405">The scoping system's name.</span></span> <span data-ttu-id="18358-406">Cette valeur correspond à la valeur de la propriété [**Name**](msvm-computersystem.md) de la classe **MSVM \_ ComputerSystem** pour l’ordinateur virtuel d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18358-406">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="18358-407">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18358-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18358-408">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="18358-408">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-409">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18358-409">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18358-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-411">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18358-411">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="18358-412">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-413">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="18358-413">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-414">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18358-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18358-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-416">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="18358-416">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="18358-417">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-417">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18358-418">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="18358-418">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18358-419">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18358-419">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18358-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18358-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18358-421">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="18358-421">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="18358-422">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18358-422">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18358-423">Notes</span><span class="sxs-lookup"><span data-stu-id="18358-423">Remarks</span></span>

<span data-ttu-id="18358-424">L’accès à la classe **MSVM \_ KvpExchangeComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="18358-424">Access to the **Msvm\_KvpExchangeComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="18358-425">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="18358-425">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="18358-426">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18358-426">Requirements</span></span>



| <span data-ttu-id="18358-427">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18358-427">Requirement</span></span> | <span data-ttu-id="18358-428">Valeur</span><span class="sxs-lookup"><span data-stu-id="18358-428">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18358-429">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18358-429">Minimum supported client</span></span><br/> | <span data-ttu-id="18358-430">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18358-430">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18358-431">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18358-431">Minimum supported server</span></span><br/> | <span data-ttu-id="18358-432">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18358-432">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18358-433">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18358-433">Namespace</span></span><br/>                | <span data-ttu-id="18358-434">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="18358-434">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18358-435">MOF</span><span class="sxs-lookup"><span data-stu-id="18358-435">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18358-436"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18358-436"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18358-437">DLL</span><span class="sxs-lookup"><span data-stu-id="18358-437">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18358-438"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18358-438"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18358-439">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18358-439">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18358-440">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="18358-440">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="18358-441">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="18358-441">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

