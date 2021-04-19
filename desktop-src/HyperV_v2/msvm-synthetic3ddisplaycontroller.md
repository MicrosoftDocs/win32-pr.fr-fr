---
description: Représente le contrôleur d’affichage 3D synthétique affecté à un ordinateur virtuel.
ms.assetid: 5679668B-7D0B-421C-92B6-8A320090DFF7
title: Msvm_Synthetic3DDisplayController, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayController
- Msvm_Synthetic3DDisplayController.RequestStateChange
- Msvm_Synthetic3DDisplayController.SetPowerState
- Msvm_Synthetic3DDisplayController.Reset
- Msvm_Synthetic3DDisplayController.EnableDevice
- Msvm_Synthetic3DDisplayController.OnlineDevice
- Msvm_Synthetic3DDisplayController.QuiesceDevice
- Msvm_Synthetic3DDisplayController.SaveProperties
- Msvm_Synthetic3DDisplayController.RestoreProperties
- Msvm_Synthetic3DDisplayController.InstanceID
- Msvm_Synthetic3DDisplayController.Caption
- Msvm_Synthetic3DDisplayController.Description
- Msvm_Synthetic3DDisplayController.ElementName
- Msvm_Synthetic3DDisplayController.InstallDate
- Msvm_Synthetic3DDisplayController.Name
- Msvm_Synthetic3DDisplayController.OperationalStatus
- Msvm_Synthetic3DDisplayController.StatusDescriptions
- Msvm_Synthetic3DDisplayController.Status
- Msvm_Synthetic3DDisplayController.HealthState
- Msvm_Synthetic3DDisplayController.CommunicationStatus
- Msvm_Synthetic3DDisplayController.DetailedStatus
- Msvm_Synthetic3DDisplayController.OperatingStatus
- Msvm_Synthetic3DDisplayController.PrimaryStatus
- Msvm_Synthetic3DDisplayController.EnabledState
- Msvm_Synthetic3DDisplayController.OtherEnabledState
- Msvm_Synthetic3DDisplayController.RequestedState
- Msvm_Synthetic3DDisplayController.EnabledDefault
- Msvm_Synthetic3DDisplayController.TimeOfLastStateChange
- Msvm_Synthetic3DDisplayController.AvailableRequestedStates
- Msvm_Synthetic3DDisplayController.TransitioningToState
- Msvm_Synthetic3DDisplayController.SystemCreationClassName
- Msvm_Synthetic3DDisplayController.SystemName
- Msvm_Synthetic3DDisplayController.CreationClassName
- Msvm_Synthetic3DDisplayController.DeviceID
- Msvm_Synthetic3DDisplayController.PowerManagementSupported
- Msvm_Synthetic3DDisplayController.PowerManagementCapabilities
- Msvm_Synthetic3DDisplayController.Availability
- Msvm_Synthetic3DDisplayController.StatusInfo
- Msvm_Synthetic3DDisplayController.LastErrorCode
- Msvm_Synthetic3DDisplayController.ErrorDescription
- Msvm_Synthetic3DDisplayController.ErrorCleared
- Msvm_Synthetic3DDisplayController.PowerOnHours
- Msvm_Synthetic3DDisplayController.TotalPowerOnHours
- Msvm_Synthetic3DDisplayController.OtherIdentifyingInfo
- Msvm_Synthetic3DDisplayController.IdentifyingDescriptions
- Msvm_Synthetic3DDisplayController.AdditionalAvailability
- Msvm_Synthetic3DDisplayController.MaxQuiesceTime
- Msvm_Synthetic3DDisplayController.TimeOfLastReset
- Msvm_Synthetic3DDisplayController.ProtocolSupported
- Msvm_Synthetic3DDisplayController.MaxNumberControlled
- Msvm_Synthetic3DDisplayController.ProtocolDescription
- Msvm_Synthetic3DDisplayController.VideoProcessor
- Msvm_Synthetic3DDisplayController.VideoMemoryType
- Msvm_Synthetic3DDisplayController.OtherVideoMemoryType
- Msvm_Synthetic3DDisplayController.NumberOfVideoPages
- Msvm_Synthetic3DDisplayController.MaxMemorySupported
- Msvm_Synthetic3DDisplayController.AcceleratorCapabilities
- Msvm_Synthetic3DDisplayController.CapabilityDescriptions
- Msvm_Synthetic3DDisplayController.OtherVideoArchitecture
- Msvm_Synthetic3DDisplayController.VideoArchitecture
- Msvm_Synthetic3DDisplayController.AllocatedGPU
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cd102fe29cf34aa0930ca264c8820868da7daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531863"
---
# <a name="msvm_synthetic3ddisplaycontroller-class"></a><span data-ttu-id="416a4-103">MSVM \_ Synthetic3DDisplayController, classe</span><span class="sxs-lookup"><span data-stu-id="416a4-103">Msvm\_Synthetic3DDisplayController class</span></span>

<span data-ttu-id="416a4-104">Représente le contrôleur d’affichage 3D synthétique affecté à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="416a4-104">Represents the synthetic 3-D display controller that is assigned to a virtual machine.</span></span> <span data-ttu-id="416a4-105">Cette classe est utilisée uniquement avec les ordinateurs virtuels qui utilisent RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="416a4-105">This class is only used with virtual machines that use RemoteFX.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="416a4-106">Lorsque vous ajoutez un contrôleur d’affichage 3D synthétique à un ordinateur virtuel, vous devez désactiver tout contrôleur d’affichage synthétique ([**MSVM \_ SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) associé à cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="416a4-106">When you add a synthetic 3-D display controller to a virtual machine, you must disable any synthetic display controller ([**Msvm\_SyntheticDisplayController**](msvm-syntheticdisplaycontroller.md)) that is attached to that virtual machine.</span></span>

 

<span data-ttu-id="416a4-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="416a4-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="416a4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="416a4-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Synthetic3DDisplayController : CIM_DisplayController
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
  string   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Synthetic Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 2048;
  uint32   MaxMemorySupported = 8388608;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
  string   AllocatedGPU;
};
```

## <a name="members"></a><span data-ttu-id="416a4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="416a4-109">Members</span></span>

<span data-ttu-id="416a4-110">La classe **MSVM \_ Synthetic3DDisplayController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="416a4-110">The **Msvm\_Synthetic3DDisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="416a4-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="416a4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="416a4-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="416a4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="416a4-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="416a4-113">Methods</span></span>

<span data-ttu-id="416a4-114">La classe **MSVM \_ Synthetic3DDisplayController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="416a4-114">The **Msvm\_Synthetic3DDisplayController** class has these methods.</span></span>



| <span data-ttu-id="416a4-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="416a4-115">Method</span></span>                 | <span data-ttu-id="416a4-116">Description</span><span class="sxs-lookup"><span data-stu-id="416a4-116">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="416a4-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="416a4-117">**EnableDevice**</span></span>       | <span data-ttu-id="416a4-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="416a4-119">**OnlineDevice**</span></span>       | <span data-ttu-id="416a4-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="416a4-121">**QuiesceDevice**</span></span>      | <span data-ttu-id="416a4-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="416a4-123">**RequestStateChange**</span></span> | <span data-ttu-id="416a4-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="416a4-125">**Reset**</span></span>              | <span data-ttu-id="416a4-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="416a4-127">**RestoreProperties**</span></span>  | <span data-ttu-id="416a4-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="416a4-129">**SaveProperties**</span></span>     | <span data-ttu-id="416a4-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="416a4-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="416a4-131">**SetPowerState**</span></span>      | <span data-ttu-id="416a4-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="416a4-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="416a4-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="416a4-133">Properties</span></span>

<span data-ttu-id="416a4-134">La classe **MSVM \_ Synthetic3DDisplayController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="416a4-134">The **Msvm\_Synthetic3DDisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="416a4-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="416a4-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-136">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-138">Les graphiques et les fonctionnalités 3D du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="416a4-138">The graphics and 3-D capabilities of the display controller.</span></span> <span data-ttu-id="416a4-139">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="416a4-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-141">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-143">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="416a4-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-144">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="416a4-144">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416a4-147">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="416a4-147">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="416a4-148">Identificateur de l’unité de traitement graphique (GPU) physique allouée à cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="416a4-148">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="416a4-149">Cette propriété s’applique uniquement aux machines virtuelles qui utilisent RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="416a4-149">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-150">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="416a4-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-151">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-153">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="416a4-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="416a4-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-155">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-157">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="416a4-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="416a4-158">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="416a4-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="416a4-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-160">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="416a4-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-162">Tableau de chaînes de forme libre qui fournissent des explications plus détaillées sur les fonctionnalités de l’accélérateur vidéo indiquées dans le tableau de propriétés **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="416a4-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** property array.</span></span> <span data-ttu-id="416a4-163">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés **AcceleratorCapabilities** situé dans le même index.</span><span class="sxs-lookup"><span data-stu-id="416a4-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** property array that is located at the same index.</span></span> <span data-ttu-id="416a4-164">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="416a4-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-168">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="416a4-168">A short description of the object.</span></span> <span data-ttu-id="416a4-169">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="416a4-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-171">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-173">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="416a4-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="416a4-174">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="416a4-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="416a4-175">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="416a4-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="416a4-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="416a4-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="416a4-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="416a4-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="416a4-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="416a4-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="416a4-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="416a4-183">)</span><span class="sxs-lookup"><span data-stu-id="416a4-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="416a4-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="416a4-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-185">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-187">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="416a4-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="416a4-188">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="416a4-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-189">**Description**</span><span class="sxs-lookup"><span data-stu-id="416a4-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-192">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="416a4-192">A description of the object.</span></span> <span data-ttu-id="416a4-193">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="416a4-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-195">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-197">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="416a4-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="416a4-198">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="416a4-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="416a4-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="416a4-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="416a4-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="416a4-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="416a4-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="416a4-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="416a4-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="416a4-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="416a4-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="416a4-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="416a4-208">)</span><span class="sxs-lookup"><span data-stu-id="416a4-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="416a4-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="416a4-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-212">Identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="416a4-212">The device identifier.</span></span> <span data-ttu-id="416a4-213">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « Microsoft :*GUID*».</span><span class="sxs-lookup"><span data-stu-id="416a4-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="416a4-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="416a4-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-217">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="416a4-217">A display name for the object.</span></span> <span data-ttu-id="416a4-218">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="416a4-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-220">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-222">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="416a4-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="416a4-223">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="416a4-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-224">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="416a4-224">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-227">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="416a4-227">The enabled and disabled states of an element.</span></span> <span data-ttu-id="416a4-228">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="416a4-228">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="416a4-229">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé) ou 3 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="416a4-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to either 2 (Enabled) or 3 (Disabled).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-230">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="416a4-230">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-231">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="416a4-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-233">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="416a4-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-237">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="416a4-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-239">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-241">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="416a4-241">The current health of the element.</span></span> <span data-ttu-id="416a4-242">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="416a4-242">This attribute expresses the health of this element but not necessarily that of its subelements.</span></span> <span data-ttu-id="416a4-243">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="416a4-243">The possible values are from 0 through 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="416a4-244">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-245">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="416a4-245">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-246">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="416a4-246">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-248">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="416a4-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="416a4-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-250">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="416a4-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-251">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-252">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="416a4-252">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="416a4-253">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-253">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-254">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="416a4-254">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-256">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="416a4-257">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="416a4-257">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="416a4-258">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="416a4-258">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="416a4-259">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-259">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-260">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="416a4-260">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-261">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="416a4-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-263">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-264">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="416a4-264">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-265">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="416a4-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-267">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="416a4-267">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="416a4-268">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-268">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-269">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="416a4-269">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-270">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="416a4-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-272">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="416a4-272">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="416a4-273">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="416a4-273">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="416a4-274">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="416a4-274">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="416a4-275">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="416a4-275">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-276">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="416a4-276">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-277">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="416a4-277">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-279">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-279">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-280">**Nom**</span><span class="sxs-lookup"><span data-stu-id="416a4-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-283">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="416a4-283">The label by which the object is known.</span></span> <span data-ttu-id="416a4-284">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-285">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="416a4-285">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-286">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="416a4-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-288">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="416a4-288">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="416a4-289">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-289">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-290">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="416a4-290">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-291">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-293">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="416a4-293">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="416a4-294">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="416a4-294">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="416a4-295">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="416a4-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="416a4-296"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="416a4-297"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="416a4-298"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="416a4-299"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="416a4-300"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="416a4-301"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="416a4-302"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="416a4-303"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="416a4-304"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="416a4-305"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="416a4-306"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="416a4-307"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="416a4-308"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="416a4-309"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="416a4-310"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="416a4-311"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="416a4-312"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="416a4-313"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="416a4-314"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="416a4-315">)</span><span class="sxs-lookup"><span data-stu-id="416a4-315">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="416a4-316">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="416a4-316">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-317">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-317">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-319">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="416a4-319">The current statuses of the object.</span></span> <span data-ttu-id="416a4-320">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-321">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="416a4-321">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-324">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="416a4-324">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="416a4-325">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="416a4-325">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="416a4-326">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="416a4-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-327">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="416a4-327">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-328">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="416a4-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-330">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="416a4-330">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-331">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="416a4-331">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-332">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-334">Chaîne qui décrit le type d’architecture vidéo lorsque la propriété **VideoArchitecture** est 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="416a4-334">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="416a4-335">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-335">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-336">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="416a4-336">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-339">Type de mémoire vidéo lorsque la propriété **VideoMemoryType** de l’instance est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="416a4-339">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="416a4-340">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-340">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-341">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="416a4-341">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-342">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-342">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-344">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-344">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-345">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="416a4-345">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-346">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="416a4-346">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-348">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-349">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="416a4-349">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-350">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="416a4-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-352">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="416a4-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-354">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-356">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="416a4-356">Provides high level status information.</span></span> <span data-ttu-id="416a4-357">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="416a4-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="416a4-358">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="416a4-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="416a4-359">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="416a4-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="416a4-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="416a4-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="416a4-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="416a4-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="416a4-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="416a4-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="416a4-366">)</span><span class="sxs-lookup"><span data-stu-id="416a4-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="416a4-367">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="416a4-367">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-368">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-370">Chaîne qui fournit des informations supplémentaires relatives au protocole pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="416a4-370">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="416a4-371">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="416a4-371">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="416a4-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-373">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-375">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="416a4-375">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="416a4-376">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="416a4-376">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-377">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="416a4-377">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-378">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-380">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="416a4-380">The last requested or desired state for the element.</span></span> <span data-ttu-id="416a4-381">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="416a4-381">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="416a4-382">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="416a4-382">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="416a4-383">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="416a4-383">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="416a4-384">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-384">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="416a4-385">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 2 (activé), 3 (désactivé) ou 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="416a4-385">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 2 (Enabled), 3 (Disabled), or 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-386">**État**</span><span class="sxs-lookup"><span data-stu-id="416a4-386">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-389">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-390">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="416a4-390">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-391">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="416a4-391">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="416a4-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-393">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="416a4-393">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="416a4-394">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="416a4-394">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-395">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="416a4-395">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-396">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-398">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-398">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-399">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="416a4-399">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-402">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="416a4-402">The scoping system's creation class name.</span></span> <span data-ttu-id="416a4-403">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="416a4-403">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="416a4-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-407">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="416a4-407">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="416a4-408">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="416a4-408">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-409">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="416a4-409">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-410">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="416a4-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-412">La dernière fois que la machine virtuelle a été mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="416a4-412">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="416a4-413">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="416a4-413">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-414">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="416a4-414">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-415">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="416a4-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-417">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="416a4-417">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="416a4-418">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-418">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-419">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="416a4-419">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-420">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="416a4-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-422">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="416a4-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-423">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="416a4-423">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-424">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-426">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="416a4-426">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="416a4-427">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="416a4-427">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="416a4-428">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="416a4-428">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-429">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-431">Spécifie l’architecture vidéo du contrôleur d’affichage utilisée pour générer le signal vidéo.</span><span class="sxs-lookup"><span data-stu-id="416a4-431">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="416a4-432">En règle générale, un processeur vidéo dédié génère le signal vidéo conformément à l’architecture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="416a4-432">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="416a4-433">Il s’agit d’un indicateur de la capacité de résolution maximale du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="416a4-433">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="416a4-434">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-434">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="416a4-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="416a4-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="416a4-436"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="416a4-437"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="416a4-438"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="416a4-439"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="416a4-440"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="416a4-441"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="416a4-442"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="416a4-443"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="416a4-444"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="416a4-445"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Mémoire tampon de trame linéaire** (11)</span><span class="sxs-lookup"><span data-stu-id="416a4-446"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="416a4-447"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="416a4-448"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="416a4-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="416a4-449"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="416a4-450">)</span><span class="sxs-lookup"><span data-stu-id="416a4-450">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="416a4-451">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="416a4-451">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-452">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="416a4-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-453">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-454">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="416a4-454">The type of video memory.</span></span> <span data-ttu-id="416a4-455">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-455">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="416a4-456">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="416a4-456">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416a4-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="416a4-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="416a4-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="416a4-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416a4-459">Chaîne qui décrit le processeur/contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="416a4-459">A string that describes the video processor/controller.</span></span> <span data-ttu-id="416a4-460">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="416a4-460">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="416a4-461">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="416a4-461">Requirements</span></span>



| <span data-ttu-id="416a4-462">Condition requise</span><span class="sxs-lookup"><span data-stu-id="416a4-462">Requirement</span></span> | <span data-ttu-id="416a4-463">Valeur</span><span class="sxs-lookup"><span data-stu-id="416a4-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416a4-464">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="416a4-464">Minimum supported client</span></span><br/> | <span data-ttu-id="416a4-465">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="416a4-465">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="416a4-466">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="416a4-466">Minimum supported server</span></span><br/> | <span data-ttu-id="416a4-467">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="416a4-467">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="416a4-468">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="416a4-468">Namespace</span></span><br/>                | <span data-ttu-id="416a4-469">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="416a4-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="416a4-470">MOF</span><span class="sxs-lookup"><span data-stu-id="416a4-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="416a4-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="416a4-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="416a4-472">DLL</span><span class="sxs-lookup"><span data-stu-id="416a4-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416a4-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="416a4-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="416a4-474">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="416a4-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416a4-475">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="416a4-475">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> </dl>

 

