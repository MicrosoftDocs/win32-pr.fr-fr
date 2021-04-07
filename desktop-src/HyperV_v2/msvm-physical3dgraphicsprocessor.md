---
description: Décrit l’unité de traitement graphique (GPU) 3D physique.
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Classe Msvm_Physical3dGraphicsProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759645"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="2502e-103">MSVM \_ Physical3dGraphicsProcessor, classe</span><span class="sxs-lookup"><span data-stu-id="2502e-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="2502e-104">Décrit l’unité de traitement graphique (GPU) 3D physique.</span><span class="sxs-lookup"><span data-stu-id="2502e-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="2502e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2502e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2502e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2502e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
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
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="2502e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="2502e-107">Members</span></span>

<span data-ttu-id="2502e-108">La classe **MSVM \_ Physical3dGraphicsProcessor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2502e-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="2502e-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2502e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2502e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2502e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2502e-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2502e-111">Methods</span></span>

<span data-ttu-id="2502e-112">La classe **MSVM \_ Physical3dGraphicsProcessor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2502e-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="2502e-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="2502e-113">Method</span></span>                 | <span data-ttu-id="2502e-114">Description</span><span class="sxs-lookup"><span data-stu-id="2502e-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="2502e-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2502e-115">**EnableDevice**</span></span>       | <span data-ttu-id="2502e-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2502e-117">**OnlineDevice**</span></span>       | <span data-ttu-id="2502e-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2502e-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="2502e-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2502e-121">**RequestStateChange**</span></span> | <span data-ttu-id="2502e-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="2502e-123">**Reset**</span></span>              | <span data-ttu-id="2502e-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="2502e-125">**RestoreProperties**</span></span>  | <span data-ttu-id="2502e-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2502e-127">**SaveProperties**</span></span>     | <span data-ttu-id="2502e-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2502e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2502e-129">**SetPowerState**</span></span>      | <span data-ttu-id="2502e-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2502e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2502e-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2502e-131">Properties</span></span>

<span data-ttu-id="2502e-132">La classe **MSVM \_ Physical3dGraphicsProcessor** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2502e-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2502e-133">**AdapterIndexID**</span><span class="sxs-lookup"><span data-stu-id="2502e-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-134">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-136">Spécifie l’identificateur d’index d’adaptateur alloué à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2502e-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2502e-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-138">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-140">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2502e-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="2502e-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-142">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="2502e-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-143">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-145">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2502e-145">The primary availability and status of the device.</span></span> <span data-ttu-id="2502e-146">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2502e-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2502e-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="2502e-151">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2502e-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-152">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="2502e-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-153">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-155">Spécifie la quantité de mémoire vidéo, en octets, disponible pour le GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-156">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2502e-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-159">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2502e-159">A short description of the object.</span></span> <span data-ttu-id="2502e-160">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-161">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2502e-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-162">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-164">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2502e-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2502e-165">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2502e-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2502e-166">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2502e-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2502e-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2502e-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="2502e-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="2502e-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="2502e-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2502e-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2502e-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2502e-174">)</span><span class="sxs-lookup"><span data-stu-id="2502e-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2502e-175">**CompatibleForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="2502e-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-176">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2502e-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-178">**true** si compatible pour la virtualisation ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2502e-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="2502e-179">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="2502e-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2502e-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2502e-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-181">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-183">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2502e-183">The scoping system's creation class name.</span></span> <span data-ttu-id="2502e-184">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2502e-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-185">**DedicatedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="2502e-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-186">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-188">Spécifie la quantité de mémoire système, en octets, dédiée au GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-189">**DedicatedVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="2502e-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-190">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-192">Spécifie la quantité de mémoire vidéo, en octets, dédiée au GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-193">**Description**</span><span class="sxs-lookup"><span data-stu-id="2502e-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-194">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-196">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="2502e-196">A description of the object.</span></span> <span data-ttu-id="2502e-197">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2502e-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-199">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-201">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2502e-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2502e-202">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2502e-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2502e-203">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2502e-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="2502e-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="2502e-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="2502e-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="2502e-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="2502e-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="2502e-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2502e-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2502e-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2502e-212">)</span><span class="sxs-lookup"><span data-stu-id="2502e-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2502e-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2502e-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-216">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2502e-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2502e-217">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2502e-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-218">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="2502e-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-221">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2502e-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2502e-222">Spécifie la prise en charge de DirectX prise en charge par le GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-223">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="2502e-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-224">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2502e-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-226">Spécifie la date de génération du pilote.</span><span class="sxs-lookup"><span data-stu-id="2502e-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-227">**DriverInstalled**</span><span class="sxs-lookup"><span data-stu-id="2502e-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-228">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2502e-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-230">Spécifie la date et l’heure d’installation du pilote.</span><span class="sxs-lookup"><span data-stu-id="2502e-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-231">**DriverModelVersion**</span><span class="sxs-lookup"><span data-stu-id="2502e-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-234">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2502e-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2502e-235">Spécifie la version du modèle de pilote.</span><span class="sxs-lookup"><span data-stu-id="2502e-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="2502e-236">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="2502e-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2502e-237">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="2502e-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-238">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-240">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2502e-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2502e-241">Spécifie le nom du fournisseur de pilotes.</span><span class="sxs-lookup"><span data-stu-id="2502e-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="2502e-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-245">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2502e-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2502e-246">Spécifie la version du pilote.</span><span class="sxs-lookup"><span data-stu-id="2502e-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2502e-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-250">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2502e-250">A display name for the object.</span></span> <span data-ttu-id="2502e-251">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2502e-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-253">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-255">Configuration par défaut ou de démarrage d’un administrateur pour la propriété **EnabledState** d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2502e-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="2502e-256">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="2502e-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-257">**EnabledForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="2502e-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-258">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2502e-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-260">Spécifie si l’adaptateur a été activé pour une utilisation avec RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="2502e-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2502e-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-262">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-264">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="2502e-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2502e-265">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2502e-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="2502e-266">Valeur</span><span class="sxs-lookup"><span data-stu-id="2502e-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2502e-267">Signification</span><span class="sxs-lookup"><span data-stu-id="2502e-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2502e-268"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="2502e-269">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2502e-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="2502e-270"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2502e-271"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="2502e-272">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2502e-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2502e-273"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2502e-274">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2502e-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="2502e-275"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="2502e-276">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="2502e-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="2502e-277"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="2502e-278">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="2502e-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="2502e-279"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="2502e-280">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="2502e-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="2502e-281"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="2502e-282">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="2502e-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="2502e-283"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="2502e-284">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="2502e-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="2502e-285"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="2502e-286">L’élément est activé, mais en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="2502e-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="2502e-287">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="2502e-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="2502e-288">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2502e-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="2502e-289">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="2502e-290">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="2502e-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="2502e-291">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2502e-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="2502e-292">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2502e-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-293">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2502e-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-295">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="2502e-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2502e-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2502e-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-300">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="2502e-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2502e-301">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="2502e-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-305">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2502e-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2502e-306">Contient l’identificateur GPU de l’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="2502e-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2502e-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-308">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-309">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-310">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2502e-310">The current health of the element.</span></span> <span data-ttu-id="2502e-311">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2502e-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-313">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2502e-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-315">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="2502e-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="2502e-316">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2502e-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-318">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2502e-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-320">Date et heure d’installation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2502e-320">The date and time when the object was installed.</span></span> <span data-ttu-id="2502e-321">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="2502e-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="2502e-322">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2502e-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-326">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="2502e-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2502e-327">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="2502e-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2502e-328">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2502e-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-330">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2502e-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-332">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2502e-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="2502e-333">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-334">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2502e-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-335">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-337">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="2502e-337">This property has been deprecated.</span></span> <span data-ttu-id="2502e-338">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-339">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2502e-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-342">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="2502e-342">The label by which the object is known.</span></span> <span data-ttu-id="2502e-343">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-344">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2502e-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-345">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-347">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2502e-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2502e-348">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2502e-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2502e-349">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2502e-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2502e-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="2502e-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="2502e-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="2502e-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="2502e-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="2502e-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="2502e-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="2502e-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="2502e-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="2502e-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="2502e-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="2502e-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="2502e-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="2502e-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="2502e-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="2502e-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="2502e-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2502e-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2502e-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2502e-369">)</span><span class="sxs-lookup"><span data-stu-id="2502e-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2502e-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2502e-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-371">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-373">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2502e-373">The current statuses of the object.</span></span> <span data-ttu-id="2502e-374">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-375">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2502e-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-378">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="2502e-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2502e-379">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="2502e-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="2502e-380">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2502e-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2502e-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-382">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2502e-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-384">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="2502e-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2502e-385">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="2502e-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-387">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-389">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2502e-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2502e-390">Spécifie la résolution de nuanceur de pixels prise en charge par le GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-391">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2502e-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-392">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-394">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2502e-394">The power management capabilities of the device.</span></span> <span data-ttu-id="2502e-395">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2502e-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-397">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2502e-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-399">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2502e-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2502e-400">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-401">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2502e-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-402">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-404">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="2502e-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2502e-405">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-406">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2502e-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-407">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-409">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="2502e-409">Provides high level status information.</span></span> <span data-ttu-id="2502e-410">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="2502e-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="2502e-411">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="2502e-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2502e-412">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="2502e-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="2502e-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="2502e-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="2502e-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="2502e-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="2502e-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2502e-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="2502e-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="2502e-419">)</span><span class="sxs-lookup"><span data-stu-id="2502e-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2502e-420">**Évaluation**</span><span class="sxs-lookup"><span data-stu-id="2502e-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-421">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-422">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2502e-423">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)</span><span class="sxs-lookup"><span data-stu-id="2502e-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="2502e-424">Spécifie l’évaluation RemoteFX du GPU pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2502e-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="2502e-425">Cette propriété n’est pas utilisée actuellement.</span><span class="sxs-lookup"><span data-stu-id="2502e-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2502e-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-427">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-429">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="2502e-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="2502e-430">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="2502e-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-431">**SharedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="2502e-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-432">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-433">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-434">Spécifie la quantité de mémoire système partagée, en octets, disponible pour le GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-435">**État**</span><span class="sxs-lookup"><span data-stu-id="2502e-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-438">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2502e-438">The current status of the object.</span></span> <span data-ttu-id="2502e-439">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-440">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2502e-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-441">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="2502e-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2502e-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-443">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2502e-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2502e-444">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2502e-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2502e-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-446">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-448">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="2502e-448">The current state of the logical device.</span></span> <span data-ttu-id="2502e-449">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2502e-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-451">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-453">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2502e-453">The scoping system's creation class name.</span></span> <span data-ttu-id="2502e-454">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2502e-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2502e-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-456">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2502e-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-457">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-458">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="2502e-458">The scoping system's name.</span></span> <span data-ttu-id="2502e-459">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2502e-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2502e-460">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2502e-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-461">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2502e-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-462">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-463">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="2502e-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2502e-464">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2502e-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2502e-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-466">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-468">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2502e-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2502e-469">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2502e-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-470">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="2502e-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-471">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2502e-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-472">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-473">Spécifie la quantité totale de mémoire vidéo, en octets, présente sur le GPU.</span><span class="sxs-lookup"><span data-stu-id="2502e-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="2502e-474">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2502e-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2502e-475">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2502e-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2502e-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2502e-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2502e-477">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="2502e-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2502e-478">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="2502e-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2502e-479">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2502e-479">Requirements</span></span>



| <span data-ttu-id="2502e-480">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2502e-480">Requirement</span></span> | <span data-ttu-id="2502e-481">Valeur</span><span class="sxs-lookup"><span data-stu-id="2502e-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2502e-482">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2502e-482">Minimum supported client</span></span><br/> | <span data-ttu-id="2502e-483">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2502e-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2502e-484">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2502e-484">Minimum supported server</span></span><br/> | <span data-ttu-id="2502e-485">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2502e-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2502e-486">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2502e-486">Namespace</span></span><br/>                | <span data-ttu-id="2502e-487">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2502e-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2502e-488">MOF</span><span class="sxs-lookup"><span data-stu-id="2502e-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2502e-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2502e-490">DLL</span><span class="sxs-lookup"><span data-stu-id="2502e-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2502e-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2502e-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

