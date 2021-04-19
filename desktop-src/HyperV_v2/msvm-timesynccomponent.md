---
description: Représente l’état du service de synchronisation de l’heure, qui est chargé de synchroniser l’heure système d’un ordinateur virtuel avec l’heure système du système d’exploitation en cours d’exécution dans le système d’exploitation de gestion.
ms.assetid: 551A81E9-E924-4A9C-965D-02FF25EE4A49
title: Classe Msvm_TimeSyncComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponent
- Msvm_TimeSyncComponent.SetPowerState
- Msvm_TimeSyncComponent.EnableDevice
- Msvm_TimeSyncComponent.OnlineDevice
- Msvm_TimeSyncComponent.QuiesceDevice
- Msvm_TimeSyncComponent.SaveProperties
- Msvm_TimeSyncComponent.RestoreProperties
- Msvm_TimeSyncComponent.InstanceID
- Msvm_TimeSyncComponent.Caption
- Msvm_TimeSyncComponent.Description
- Msvm_TimeSyncComponent.ElementName
- Msvm_TimeSyncComponent.InstallDate
- Msvm_TimeSyncComponent.Name
- Msvm_TimeSyncComponent.OperationalStatus
- Msvm_TimeSyncComponent.StatusDescriptions
- Msvm_TimeSyncComponent.Status
- Msvm_TimeSyncComponent.HealthState
- Msvm_TimeSyncComponent.CommunicationStatus
- Msvm_TimeSyncComponent.DetailedStatus
- Msvm_TimeSyncComponent.OperatingStatus
- Msvm_TimeSyncComponent.PrimaryStatus
- Msvm_TimeSyncComponent.EnabledState
- Msvm_TimeSyncComponent.OtherEnabledState
- Msvm_TimeSyncComponent.RequestedState
- Msvm_TimeSyncComponent.EnabledDefault
- Msvm_TimeSyncComponent.TimeOfLastStateChange
- Msvm_TimeSyncComponent.AvailableRequestedStates
- Msvm_TimeSyncComponent.TransitioningToState
- Msvm_TimeSyncComponent.SystemCreationClassName
- Msvm_TimeSyncComponent.SystemName
- Msvm_TimeSyncComponent.CreationClassName
- Msvm_TimeSyncComponent.DeviceID
- Msvm_TimeSyncComponent.PowerManagementSupported
- Msvm_TimeSyncComponent.PowerManagementCapabilities
- Msvm_TimeSyncComponent.Availability
- Msvm_TimeSyncComponent.StatusInfo
- Msvm_TimeSyncComponent.LastErrorCode
- Msvm_TimeSyncComponent.ErrorDescription
- Msvm_TimeSyncComponent.ErrorCleared
- Msvm_TimeSyncComponent.OtherIdentifyingInfo
- Msvm_TimeSyncComponent.PowerOnHours
- Msvm_TimeSyncComponent.TotalPowerOnHours
- Msvm_TimeSyncComponent.IdentifyingDescriptions
- Msvm_TimeSyncComponent.AdditionalAvailability
- Msvm_TimeSyncComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea9a33d665a315861d9e6c51fd529f10f07b4aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534386"
---
# <a name="msvm_timesynccomponent-class"></a><span data-ttu-id="18d54-103">MSVM \_ TimeSyncComponent, classe</span><span class="sxs-lookup"><span data-stu-id="18d54-103">Msvm\_TimeSyncComponent class</span></span>

<span data-ttu-id="18d54-104">Représente l’état du service de synchronisation de l’heure, qui est chargé de synchroniser l’heure système d’un ordinateur virtuel avec l’heure système du système d’exploitation en cours d’exécution dans le système d’exploitation de gestion.</span><span class="sxs-lookup"><span data-stu-id="18d54-104">Represents the state of the time synchronization service, which is responsible for synchronizing the system time of a virtual machine with the system time of the operating system running in the management operating system.</span></span>

<span data-ttu-id="18d54-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="18d54-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d54-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18d54-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Time Synchronization";
  string   Description = "Microsoft Time Synchronization Service";
  string   ElementName = "Time Synchronization";
  datetime InstallDate;
  string   Name = "Time Synchronization";
  uint16   OperationalStatus[] = { 2 };
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TimeSyncComponent";
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

## <a name="members"></a><span data-ttu-id="18d54-107">Membres</span><span class="sxs-lookup"><span data-stu-id="18d54-107">Members</span></span>

<span data-ttu-id="18d54-108">La classe **MSVM \_ TimeSyncComponent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18d54-108">The **Msvm\_TimeSyncComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="18d54-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18d54-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="18d54-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18d54-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="18d54-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="18d54-111">Methods</span></span>

<span data-ttu-id="18d54-112">La classe **MSVM \_ TimeSyncComponent** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="18d54-112">The **Msvm\_TimeSyncComponent** class has these methods.</span></span>



| <span data-ttu-id="18d54-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="18d54-113">Method</span></span>                                                                  | <span data-ttu-id="18d54-114">Description</span><span class="sxs-lookup"><span data-stu-id="18d54-114">Description</span></span>                              |
|:------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="18d54-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="18d54-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="18d54-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d54-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18d54-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="18d54-117">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="18d54-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d54-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18d54-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="18d54-119">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="18d54-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d54-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="18d54-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="18d54-121">**RequestStateChange**</span></span>](msvm-timesynccomponent-requeststatechange.md) | <span data-ttu-id="18d54-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="18d54-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="18d54-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="18d54-123">**Reset**</span></span>](msvm-timesynccomponent-reset.md)                           | <span data-ttu-id="18d54-124">Réinitialise le composant.</span><span class="sxs-lookup"><span data-stu-id="18d54-124">Resets the component.</span></span><br/>         |
| <span data-ttu-id="18d54-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="18d54-125">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="18d54-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d54-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18d54-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="18d54-127">**SaveProperties**</span></span>                                                      | <span data-ttu-id="18d54-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d54-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="18d54-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="18d54-129">**SetPowerState**</span></span>                                                       | <span data-ttu-id="18d54-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18d54-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="18d54-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18d54-131">Properties</span></span>

<span data-ttu-id="18d54-132">La classe **MSVM \_ TimeSyncComponent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="18d54-132">The **Msvm\_TimeSyncComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18d54-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="18d54-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-134">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-136">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d54-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="18d54-137">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="18d54-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-138">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="18d54-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-141">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d54-141">The primary availability and status of the device.</span></span> <span data-ttu-id="18d54-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18d54-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="18d54-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-143">Value</span></span>                                                                        | <span data-ttu-id="18d54-144">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-144">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18d54-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="18d54-146">Non applicable</span><span class="sxs-lookup"><span data-stu-id="18d54-146">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18d54-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="18d54-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="18d54-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="18d54-151">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="18d54-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="18d54-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-155">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18d54-155">A short description of the object.</span></span> <span data-ttu-id="18d54-156">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-157">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="18d54-157">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-158">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-160">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="18d54-160">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="18d54-161">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18d54-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18d54-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18d54-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18d54-163"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="18d54-164"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="18d54-165"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="18d54-166"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="18d54-167"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18d54-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18d54-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18d54-170">)</span><span class="sxs-lookup"><span data-stu-id="18d54-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18d54-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18d54-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-172">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-174">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18d54-174">The scoping system's creation class name.</span></span> <span data-ttu-id="18d54-175">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18d54-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-176">**Description**</span><span class="sxs-lookup"><span data-stu-id="18d54-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-179">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="18d54-179">A description of the object.</span></span> <span data-ttu-id="18d54-180">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="18d54-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-182">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-184">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="18d54-184">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="18d54-185">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18d54-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18d54-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18d54-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="18d54-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="18d54-188"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="18d54-189"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="18d54-190"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="18d54-191"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="18d54-192"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18d54-193"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18d54-194"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18d54-195">)</span><span class="sxs-lookup"><span data-stu-id="18d54-195">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18d54-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="18d54-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-199">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18d54-199">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="18d54-200">Cette propriété est héritée [**de CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*VMGUID* \\ *GUID*», où *VMGUID* est la propriété **Name** de l’instance [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associée à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="18d54-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-201">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="18d54-201">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-204">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18d54-204">A display name for the object.</span></span> <span data-ttu-id="18d54-205">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-206">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="18d54-206">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-207">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-209">Configuration par défaut ou de démarrage d’un administrateur pour **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="18d54-209">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="18d54-210">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18d54-210">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18d54-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-211">Value</span></span>                                                                        | <span data-ttu-id="18d54-212">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-212">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="18d54-213"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-213"><dt>7</dt></span></span> </dl> | <span data-ttu-id="18d54-214">Pas de valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="18d54-214">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18d54-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="18d54-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-216">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-218">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="18d54-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="18d54-219">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et a la valeur 2 (activé) ou 3 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="18d54-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="18d54-220">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-220">Value</span></span>                                                                        | <span data-ttu-id="18d54-221">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-221">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="18d54-222"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-222"><dt>2</dt></span></span> </dl> | <span data-ttu-id="18d54-223">activé</span><span class="sxs-lookup"><span data-stu-id="18d54-223">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="18d54-224"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-224"><dt>3</dt></span></span> </dl> | <span data-ttu-id="18d54-225">Désactivé</span><span class="sxs-lookup"><span data-stu-id="18d54-225">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18d54-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="18d54-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-227">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d54-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-229">Indique si l’erreur signalée dans la propriété **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="18d54-229">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="18d54-230">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="18d54-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-234">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans la propriété **LastErrorCode** et des informations sur toutes les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="18d54-234">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="18d54-235">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-236">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="18d54-236">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-237">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-239">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18d54-239">The current health of the element.</span></span> <span data-ttu-id="18d54-240">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="18d54-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-241">Value</span></span>                                                                        | <span data-ttu-id="18d54-242">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-242">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="18d54-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-243"><dt>5</dt></span></span> </dl> | <span data-ttu-id="18d54-244">Ok</span><span class="sxs-lookup"><span data-stu-id="18d54-244">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18d54-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18d54-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-246">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18d54-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-248">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="18d54-248">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="18d54-249">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-250">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="18d54-250">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-251">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18d54-251">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-253">Date et heure auxquelles le service d’intégration a été installé sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="18d54-253">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="18d54-254">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-255">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="18d54-255">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-256">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18d54-258">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="18d54-258">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="18d54-259">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="18d54-259">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="18d54-260">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-261">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="18d54-261">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-262">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18d54-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-264">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18d54-264">The last error code reported by the logical device.</span></span> <span data-ttu-id="18d54-265">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-266">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="18d54-266">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-267">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18d54-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-269">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="18d54-269">This property has been deprecated.</span></span> <span data-ttu-id="18d54-270">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18d54-270">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-271">**Nom**</span><span class="sxs-lookup"><span data-stu-id="18d54-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-274">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="18d54-274">The label by which the object is known.</span></span> <span data-ttu-id="18d54-275">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-275">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-276">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="18d54-276">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-277">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-279">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="18d54-279">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="18d54-280">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18d54-280">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18d54-281">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18d54-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18d54-282"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="18d54-283"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="18d54-284"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="18d54-285"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="18d54-286"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="18d54-287"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="18d54-288"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="18d54-289"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="18d54-290"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="18d54-291"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="18d54-292"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="18d54-293"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="18d54-294"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="18d54-295"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="18d54-296"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="18d54-297"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="18d54-298"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18d54-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18d54-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18d54-301">)</span><span class="sxs-lookup"><span data-stu-id="18d54-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18d54-302">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="18d54-302">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-303">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-305">État actuel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18d54-305">The current status of the element.</span></span> <span data-ttu-id="18d54-306">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-306">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="18d54-307">Les valeurs possibles pour la valeur de la propriété **OperationalStatus** 0 sont les suivantes \[ \] .</span><span class="sxs-lookup"><span data-stu-id="18d54-307">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="18d54-308">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-308">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="18d54-309">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-309">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18d54-310"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-310"><dt>{ 2 }</dt></span></span> </dl>                                                                                                                                                                                                    |                                                                                                                                                                                                                                          |
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="18d54-311"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-311"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="18d54-312">Le service fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="18d54-312">The service is operating normally.</span></span> <span data-ttu-id="18d54-313">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18d54-313">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="18d54-314"><dt>**Dégradé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-314"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="18d54-315">Le service fonctionne normalement, mais le service invité a négocié une version de protocole de communication compatible.</span><span class="sxs-lookup"><span data-stu-id="18d54-315">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="18d54-316">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18d54-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="18d54-317"><dt>**Erreur non récupérable**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-317"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="18d54-318">L’invité ne prend pas en charge une version de protocole compatible.</span><span class="sxs-lookup"><span data-stu-id="18d54-318">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="18d54-319">Les  \[ valeurs des \] Propriétés OperationalStatus 1 et **StatusDescriptions** \[ 1 \] peuvent contenir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18d54-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="18d54-320"><dt>**Aucun contact**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-320"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="18d54-321">Le service invité n’est pas installé ou n’a pas encore été contacté.</span><span class="sxs-lookup"><span data-stu-id="18d54-321">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="18d54-322"><dt>**Communication perdue**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-322"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="18d54-323">Le service invité ne répond plus normalement.</span><span class="sxs-lookup"><span data-stu-id="18d54-323">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="18d54-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="18d54-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-327">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="18d54-327">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="18d54-328">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="18d54-328">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="18d54-329">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et a toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="18d54-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="18d54-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-331">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18d54-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-333">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="18d54-333">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="18d54-334">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) et prend toujours la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="18d54-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="18d54-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-336">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-337">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-338">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="18d54-338">The power management capabilities of the device.</span></span> <span data-ttu-id="18d54-339">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-339">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-340">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="18d54-340">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-341">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="18d54-341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-343">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="18d54-343">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="18d54-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-345">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="18d54-345">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-346">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18d54-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-348">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="18d54-348">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="18d54-349">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-350">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="18d54-350">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-351">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-353">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="18d54-353">Provides high level status information.</span></span> <span data-ttu-id="18d54-354">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="18d54-354">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="18d54-355">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="18d54-355">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="18d54-356">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="18d54-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="18d54-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="18d54-358"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="18d54-359"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="18d54-360"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="18d54-361"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="18d54-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="18d54-362"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="18d54-363">)</span><span class="sxs-lookup"><span data-stu-id="18d54-363">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="18d54-364">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="18d54-364">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-365">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-367">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="18d54-367">The last requested or desired state for the element.</span></span> <span data-ttu-id="18d54-368">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18d54-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18d54-369">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-369">Value</span></span>                                                                         | <span data-ttu-id="18d54-370">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-370">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18d54-371"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-371"><dt>12</dt></span></span> </dl> | <span data-ttu-id="18d54-372">Non applicable</span><span class="sxs-lookup"><span data-stu-id="18d54-372">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18d54-373">**État**</span><span class="sxs-lookup"><span data-stu-id="18d54-373">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-374">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-376">Chaîne qui spécifie l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="18d54-376">A string that specifies the current status of the object.</span></span> <span data-ttu-id="18d54-377">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) mais n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-378">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="18d54-378">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-379">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="18d54-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18d54-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-381">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="18d54-381">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="18d54-382">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="18d54-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="18d54-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-384">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-386">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="18d54-386">The current state of the logical device.</span></span> <span data-ttu-id="18d54-387">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-387">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="18d54-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-389">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-391">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18d54-391">The creation class name of the scoping system.</span></span> <span data-ttu-id="18d54-392">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18d54-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-393">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="18d54-393">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="18d54-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-396">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="18d54-396">The name of the scoping system.</span></span> <span data-ttu-id="18d54-397">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="18d54-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="18d54-398">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="18d54-398">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-399">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18d54-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-401">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="18d54-401">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="18d54-402">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="18d54-402">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-403">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="18d54-403">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-404">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="18d54-404">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-406">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="18d54-406">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="18d54-407">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="18d54-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="18d54-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="18d54-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18d54-409">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="18d54-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="18d54-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18d54-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="18d54-411">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="18d54-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="18d54-412">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="18d54-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="18d54-413">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-413">Value</span></span>                                                                         | <span data-ttu-id="18d54-414">Signification</span><span class="sxs-lookup"><span data-stu-id="18d54-414">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="18d54-415"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-415"><dt>12</dt></span></span> </dl> | <span data-ttu-id="18d54-416">Non applicable</span><span class="sxs-lookup"><span data-stu-id="18d54-416">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18d54-417">Notes</span><span class="sxs-lookup"><span data-stu-id="18d54-417">Remarks</span></span>

<span data-ttu-id="18d54-418">L’accès à la classe **MSVM \_ TimeSyncComponent** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="18d54-418">Access to the **Msvm\_TimeSyncComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="18d54-419">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="18d54-419">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="18d54-420">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18d54-420">Requirements</span></span>



| <span data-ttu-id="18d54-421">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18d54-421">Requirement</span></span> | <span data-ttu-id="18d54-422">Valeur</span><span class="sxs-lookup"><span data-stu-id="18d54-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d54-423">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d54-423">Minimum supported client</span></span><br/> | <span data-ttu-id="18d54-424">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18d54-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="18d54-425">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18d54-425">Minimum supported server</span></span><br/> | <span data-ttu-id="18d54-426">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18d54-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18d54-427">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="18d54-427">Namespace</span></span><br/>                | <span data-ttu-id="18d54-428">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="18d54-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="18d54-429">MOF</span><span class="sxs-lookup"><span data-stu-id="18d54-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18d54-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18d54-431">DLL</span><span class="sxs-lookup"><span data-stu-id="18d54-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18d54-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18d54-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="18d54-433">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d54-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d54-434">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="18d54-434">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="18d54-435">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="18d54-435">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

