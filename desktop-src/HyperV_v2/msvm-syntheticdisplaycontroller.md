---
description: Représente l’état du contrôleur d’affichage synthétique qui est présent dans chaque configuration d’ordinateur virtuel.
ms.assetid: E496B887-9032-43D8-A7D2-67BB77342AFD
title: Msvm_SyntheticDisplayController, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayController
- Msvm_SyntheticDisplayController.SetPowerState
- Msvm_SyntheticDisplayController.EnableDevice
- Msvm_SyntheticDisplayController.OnlineDevice
- Msvm_SyntheticDisplayController.QuiesceDevice
- Msvm_SyntheticDisplayController.SaveProperties
- Msvm_SyntheticDisplayController.RestoreProperties
- Msvm_SyntheticDisplayController.InstanceID
- Msvm_SyntheticDisplayController.Caption
- Msvm_SyntheticDisplayController.Description
- Msvm_SyntheticDisplayController.ElementName
- Msvm_SyntheticDisplayController.InstallDate
- Msvm_SyntheticDisplayController.Name
- Msvm_SyntheticDisplayController.OperationalStatus
- Msvm_SyntheticDisplayController.StatusDescriptions
- Msvm_SyntheticDisplayController.Status
- Msvm_SyntheticDisplayController.HealthState
- Msvm_SyntheticDisplayController.CommunicationStatus
- Msvm_SyntheticDisplayController.DetailedStatus
- Msvm_SyntheticDisplayController.OperatingStatus
- Msvm_SyntheticDisplayController.PrimaryStatus
- Msvm_SyntheticDisplayController.EnabledState
- Msvm_SyntheticDisplayController.OtherEnabledState
- Msvm_SyntheticDisplayController.RequestedState
- Msvm_SyntheticDisplayController.EnabledDefault
- Msvm_SyntheticDisplayController.TimeOfLastStateChange
- Msvm_SyntheticDisplayController.AvailableRequestedStates
- Msvm_SyntheticDisplayController.TransitioningToState
- Msvm_SyntheticDisplayController.SystemCreationClassName
- Msvm_SyntheticDisplayController.SystemName
- Msvm_SyntheticDisplayController.CreationClassName
- Msvm_SyntheticDisplayController.DeviceID
- Msvm_SyntheticDisplayController.PowerManagementSupported
- Msvm_SyntheticDisplayController.PowerManagementCapabilities
- Msvm_SyntheticDisplayController.Availability
- Msvm_SyntheticDisplayController.StatusInfo
- Msvm_SyntheticDisplayController.LastErrorCode
- Msvm_SyntheticDisplayController.ErrorDescription
- Msvm_SyntheticDisplayController.ErrorCleared
- Msvm_SyntheticDisplayController.PowerOnHours
- Msvm_SyntheticDisplayController.TotalPowerOnHours
- Msvm_SyntheticDisplayController.OtherIdentifyingInfo
- Msvm_SyntheticDisplayController.IdentifyingDescriptions
- Msvm_SyntheticDisplayController.AdditionalAvailability
- Msvm_SyntheticDisplayController.MaxQuiesceTime
- Msvm_SyntheticDisplayController.TimeOfLastReset
- Msvm_SyntheticDisplayController.ProtocolSupported
- Msvm_SyntheticDisplayController.MaxNumberControlled
- Msvm_SyntheticDisplayController.ProtocolDescription
- Msvm_SyntheticDisplayController.VideoProcessor
- Msvm_SyntheticDisplayController.VideoMemoryType
- Msvm_SyntheticDisplayController.OtherVideoMemoryType
- Msvm_SyntheticDisplayController.NumberOfVideoPages
- Msvm_SyntheticDisplayController.MaxMemorySupported
- Msvm_SyntheticDisplayController.AcceleratorCapabilities
- Msvm_SyntheticDisplayController.CapabilityDescriptions
- Msvm_SyntheticDisplayController.OtherVideoArchitecture
- Msvm_SyntheticDisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7f566bf2a75b3ed4f503da245d7b6ce428dce5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863558"
---
# <a name="msvm_syntheticdisplaycontroller-class"></a><span data-ttu-id="4693b-103">MSVM \_ SyntheticDisplayController, classe</span><span class="sxs-lookup"><span data-stu-id="4693b-103">Msvm\_SyntheticDisplayController class</span></span>

<span data-ttu-id="4693b-104">Représente l’état du contrôleur d’affichage synthétique qui est présent dans chaque configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4693b-104">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="4693b-105">Un seul contrôleur d’affichage peut être actif sur une machine virtuelle à tout moment et le contrôleur synthétique ne peut être activé que si le système d’exploitation invité a chargé les services d’accélération vidéo requis.</span><span class="sxs-lookup"><span data-stu-id="4693b-105">Only one display controller can be active in a virtual machine at any time and the synthetic controller can be activated only when the guest operating system has loaded the required video acceleration services.</span></span>

<span data-ttu-id="4693b-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4693b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4693b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4693b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Synthetic Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_SyntheticDisplayController";
  string   DeviceID = "Microsoft:GUID";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 1024;
  uint32   MaxMemorySupported = 4194304;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="4693b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4693b-108">Members</span></span>

<span data-ttu-id="4693b-109">La classe **MSVM \_ SyntheticDisplayController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4693b-109">The **Msvm\_SyntheticDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="4693b-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4693b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4693b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4693b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4693b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4693b-112">Methods</span></span>

<span data-ttu-id="4693b-113">La classe **MSVM \_ SyntheticDisplayController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4693b-113">The **Msvm\_SyntheticDisplayController** class has these methods.</span></span>



| <span data-ttu-id="4693b-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="4693b-114">Method</span></span>                                                                           | <span data-ttu-id="4693b-115">Description</span><span class="sxs-lookup"><span data-stu-id="4693b-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="4693b-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="4693b-116">**EnableDevice**</span></span>                                                                 | <span data-ttu-id="4693b-117">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4693b-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4693b-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="4693b-118">**OnlineDevice**</span></span>                                                                 | <span data-ttu-id="4693b-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4693b-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4693b-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="4693b-120">**QuiesceDevice**</span></span>                                                                | <span data-ttu-id="4693b-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4693b-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="4693b-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="4693b-122">**RequestStateChange**</span></span>](msvm-syntheticdisplaycontroller-requeststatechange.md) | <span data-ttu-id="4693b-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="4693b-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="4693b-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="4693b-124">**Reset**</span></span>](msvm-syntheticdisplaycontroller-reset.md)                           | <span data-ttu-id="4693b-125">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="4693b-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="4693b-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="4693b-126">**RestoreProperties**</span></span>                                                            | <span data-ttu-id="4693b-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4693b-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4693b-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="4693b-128">**SaveProperties**</span></span>                                                               | <span data-ttu-id="4693b-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4693b-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="4693b-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4693b-130">**SetPowerState**</span></span>                                                                | <span data-ttu-id="4693b-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4693b-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4693b-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4693b-132">Properties</span></span>

<span data-ttu-id="4693b-133">La classe **MSVM \_ SyntheticDisplayController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4693b-133">The **Msvm\_SyntheticDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4693b-134">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4693b-134">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-135">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-137">Les graphiques et les fonctionnalités 3D du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4693b-137">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="4693b-138">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur 2 (Accélérateur graphique).</span><span class="sxs-lookup"><span data-stu-id="4693b-138">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (Graphics Accelerator).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="4693b-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-140">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="4693b-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-143">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="4693b-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-146">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="4693b-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="4693b-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="4693b-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="4693b-151">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4693b-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-152">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4693b-152">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-153">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4693b-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-155">Tableau de chaînes de forme libre qui fournissent des explications plus détaillées sur les fonctionnalités de l’accélérateur vidéo indiquées dans le tableau de propriétés **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4693b-155">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="4693b-156">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés **AcceleratorCapabilities** situé dans le même index.</span><span class="sxs-lookup"><span data-stu-id="4693b-156">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="4693b-157">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur « Graphic Accelerator ».</span><span class="sxs-lookup"><span data-stu-id="4693b-157">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Graphics Accelerator".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-158">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4693b-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-161">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4693b-161">A short description of the object.</span></span> <span data-ttu-id="4693b-162">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « contrôleur d’affichage ».</span><span class="sxs-lookup"><span data-stu-id="4693b-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-163">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4693b-163">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-164">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-166">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4693b-166">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4693b-167">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4693b-167">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4693b-168">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4693b-168">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4693b-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4693b-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4693b-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="4693b-171"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="4693b-172"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="4693b-173"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4693b-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4693b-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4693b-176">)</span><span class="sxs-lookup"><span data-stu-id="4693b-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4693b-177">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4693b-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-180">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="4693b-180">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4693b-181">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ SyntheticDisplayController ».</span><span class="sxs-lookup"><span data-stu-id="4693b-181">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_SyntheticDisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-182">**Description**</span><span class="sxs-lookup"><span data-stu-id="4693b-182">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-185">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="4693b-185">A description of the object.</span></span> <span data-ttu-id="4693b-186">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « contrôleur d’affichage synthétique Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="4693b-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Synthetic Display Controller".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-187">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4693b-187">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-188">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-190">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4693b-190">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4693b-191">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4693b-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4693b-192">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4693b-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4693b-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="4693b-193"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="4693b-194"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="4693b-195"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="4693b-196"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="4693b-197"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="4693b-198"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4693b-199"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4693b-200"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4693b-201">)</span><span class="sxs-lookup"><span data-stu-id="4693b-201">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4693b-202">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4693b-202">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-203">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-205">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID*».</span><span class="sxs-lookup"><span data-stu-id="4693b-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-206">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4693b-206">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-209">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4693b-209">A display name for the object.</span></span> <span data-ttu-id="4693b-210">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « Display Controller » par défaut.</span><span class="sxs-lookup"><span data-stu-id="4693b-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Display Controller" by default.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-211">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="4693b-211">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-214">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4693b-214">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="4693b-215">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="4693b-215">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-216">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="4693b-216">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-219">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4693b-219">The enabled and disabled states of an element.</span></span> <span data-ttu-id="4693b-220">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="4693b-220">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="4693b-221">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé) ou 3 (désactivée).</span><span class="sxs-lookup"><span data-stu-id="4693b-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-222">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="4693b-222">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-223">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4693b-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-225">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-225">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-226">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4693b-226">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-229">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-229">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-230">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4693b-230">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-231">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-233">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4693b-233">The current health of the element.</span></span> <span data-ttu-id="4693b-234">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="4693b-234">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="4693b-235">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="4693b-235">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="4693b-236">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="4693b-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-237">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4693b-237">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-238">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4693b-238">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-240">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4693b-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-241">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4693b-241">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-242">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4693b-242">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-244">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="4693b-244">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="4693b-245">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4693b-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4693b-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4693b-249">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4693b-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4693b-250">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4693b-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4693b-251">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4693b-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-252">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="4693b-252">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-253">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4693b-253">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-255">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-256">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="4693b-256">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-257">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4693b-257">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-259">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="4693b-259">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="4693b-260">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur 4 194 304 (0x400000).</span><span class="sxs-lookup"><span data-stu-id="4693b-260">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 4,194,304 (0x400000).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-261">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="4693b-261">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-262">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4693b-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-264">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4693b-264">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="4693b-265">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="4693b-265">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="4693b-266">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="4693b-266">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="4693b-267">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="4693b-267">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-268">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="4693b-268">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-269">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4693b-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-271">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-272">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4693b-272">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-275">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4693b-275">The label by which the object is known.</span></span> <span data-ttu-id="4693b-276">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="4693b-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-277">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="4693b-277">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-278">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4693b-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-280">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="4693b-280">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="4693b-281">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur 1024.</span><span class="sxs-lookup"><span data-stu-id="4693b-281">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 1024.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4693b-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-285">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4693b-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4693b-286">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4693b-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4693b-287">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4693b-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4693b-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4693b-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="4693b-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="4693b-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="4693b-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="4693b-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="4693b-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="4693b-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="4693b-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="4693b-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="4693b-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="4693b-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="4693b-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="4693b-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="4693b-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="4693b-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="4693b-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="4693b-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4693b-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4693b-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4693b-307">)</span><span class="sxs-lookup"><span data-stu-id="4693b-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4693b-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4693b-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-309">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-311">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4693b-311">The current statuses of the object.</span></span> <span data-ttu-id="4693b-312">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="4693b-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="4693b-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-314">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-316">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4693b-316">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="4693b-317">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="4693b-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="4693b-318">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4693b-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4693b-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-320">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4693b-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-322">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4693b-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-323">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="4693b-323">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-326">Chaîne qui décrit le type d’architecture vidéo lorsque la propriété **VideoArchitecture** est 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="4693b-326">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="4693b-327">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4693b-327">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-328">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="4693b-328">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-331">Type de mémoire vidéo lorsque la propriété **VideoMemoryType** de l’instance est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4693b-331">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="4693b-332">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4693b-332">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4693b-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-334">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-336">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-336">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-337">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="4693b-337">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-338">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4693b-338">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-340">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-341">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4693b-341">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4693b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-345">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4693b-345">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-346">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-348">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="4693b-348">Provides high level status information.</span></span> <span data-ttu-id="4693b-349">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="4693b-349">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="4693b-350">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="4693b-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4693b-351">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4693b-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="4693b-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4693b-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="4693b-353"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="4693b-354"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="4693b-355"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4693b-356"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4693b-357"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4693b-358">)</span><span class="sxs-lookup"><span data-stu-id="4693b-358">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4693b-359">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="4693b-359">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-360">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-362">Chaîne qui fournit des informations supplémentaires relatives au protocole pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="4693b-362">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="4693b-363">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)et est toujours définie sur « video ».</span><span class="sxs-lookup"><span data-stu-id="4693b-363">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to "Video".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-364">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="4693b-364">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-365">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-365">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-367">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="4693b-367">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="4693b-368">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller)et est toujours définie sur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="4693b-368">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-369">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="4693b-369">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-370">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-372">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="4693b-372">The last requested or desired state for the element.</span></span> <span data-ttu-id="4693b-373">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="4693b-373">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="4693b-374">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="4693b-374">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="4693b-375">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="4693b-375">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="4693b-376">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-376">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="4693b-377">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est définie sur 2 (activé), 3 (désactivé) ou 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="4693b-377">This property is inherited from **CIM\_EnabledLogicalElement**, and it is set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-378">**État**</span><span class="sxs-lookup"><span data-stu-id="4693b-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-381">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-381">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-382">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4693b-382">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-383">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="4693b-383">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4693b-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-385">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4693b-385">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="4693b-386">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="4693b-386">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-387">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4693b-387">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-388">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-390">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-390">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4693b-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-392">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-394">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4693b-394">The scoping system's creation class name.</span></span> <span data-ttu-id="4693b-395">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="4693b-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="4693b-396">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4693b-396">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-399">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="4693b-399">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="4693b-400">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="4693b-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-401">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="4693b-401">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-402">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4693b-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-404">La dernière fois que la machine virtuelle a été mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="4693b-404">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="4693b-405">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="4693b-405">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-406">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="4693b-406">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-407">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4693b-407">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-409">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4693b-409">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="4693b-410">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4693b-410">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-411">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="4693b-411">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-412">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4693b-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-414">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4693b-414">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-415">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="4693b-415">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-416">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-417">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-418">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="4693b-418">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="4693b-419">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="4693b-419">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4693b-420">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="4693b-420">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-421">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-423">Spécifie l’architecture vidéo du contrôleur d’affichage utilisée pour générer le signal vidéo.</span><span class="sxs-lookup"><span data-stu-id="4693b-423">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="4693b-424">En règle générale, un processeur vidéo dédié génère le signal vidéo conformément à l’architecture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4693b-424">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="4693b-425">Il s’agit d’un indicateur de la capacité de résolution maximale du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="4693b-425">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="4693b-426">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4693b-426">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="4693b-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="4693b-427"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="4693b-428"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="4693b-429"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="4693b-430"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="4693b-431"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="4693b-432"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="4693b-433"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="4693b-434"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="4693b-435"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="4693b-436"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="4693b-437"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Mémoire tampon de trame linéaire** (11)</span><span class="sxs-lookup"><span data-stu-id="4693b-438"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="4693b-439"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4693b-440"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4693b-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="4693b-441"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="4693b-442">)</span><span class="sxs-lookup"><span data-stu-id="4693b-442">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4693b-443">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="4693b-443">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-444">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4693b-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-446">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="4693b-446">The type of video memory.</span></span> <span data-ttu-id="4693b-447">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur 2 (VRAM).</span><span class="sxs-lookup"><span data-stu-id="4693b-447">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to 2 (VRAM).</span></span>

</dd> <dt>

<span data-ttu-id="4693b-448">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="4693b-448">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4693b-449">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4693b-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4693b-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4693b-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4693b-451">Chaîne qui décrit le processeur/contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="4693b-451">A string that describes the video processor/controller.</span></span> <span data-ttu-id="4693b-452">Cette propriété est héritée de [**CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))et est toujours définie sur « processeur vidéo synthétique ».</span><span class="sxs-lookup"><span data-stu-id="4693b-452">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)), and it is always set to "Synthetic Video Processor".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4693b-453">Notes</span><span class="sxs-lookup"><span data-stu-id="4693b-453">Remarks</span></span>

<span data-ttu-id="4693b-454">L’accès à la classe **MSVM \_ SyntheticDisplayController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="4693b-454">Access to the **Msvm\_SyntheticDisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4693b-455">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4693b-455">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4693b-456">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4693b-456">Requirements</span></span>



| <span data-ttu-id="4693b-457">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4693b-457">Requirement</span></span> | <span data-ttu-id="4693b-458">Valeur</span><span class="sxs-lookup"><span data-stu-id="4693b-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4693b-459">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4693b-459">Minimum supported client</span></span><br/> | <span data-ttu-id="4693b-460">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4693b-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4693b-461">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4693b-461">Minimum supported server</span></span><br/> | <span data-ttu-id="4693b-462">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4693b-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4693b-463">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4693b-463">Namespace</span></span><br/>                | <span data-ttu-id="4693b-464">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4693b-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4693b-465">MOF</span><span class="sxs-lookup"><span data-stu-id="4693b-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4693b-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4693b-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4693b-467">DLL</span><span class="sxs-lookup"><span data-stu-id="4693b-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4693b-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4693b-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4693b-469">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4693b-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4693b-470">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="4693b-470">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="4693b-471">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4693b-471">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4693b-472">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="4693b-472">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

