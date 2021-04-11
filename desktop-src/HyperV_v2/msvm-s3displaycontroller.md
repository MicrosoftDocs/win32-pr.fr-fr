---
description: Représente l’état du contrôleur S3 émulé qui est présent dans chaque configuration d’ordinateur virtuel.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Msvm_S3DisplayController, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115982"
---
# <a name="msvm_s3displaycontroller-class"></a><span data-ttu-id="58bee-103">MSVM \_ S3DisplayController, classe</span><span class="sxs-lookup"><span data-stu-id="58bee-103">Msvm\_S3DisplayController class</span></span>

<span data-ttu-id="58bee-104">Représente l’état du contrôleur S3 émulé qui est présent dans chaque configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="58bee-104">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span> <span data-ttu-id="58bee-105">Un seul contrôleur d’affichage peut être actif sur une machine virtuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="58bee-105">Only one display controller can be active in a virtual machine at any time.</span></span>

> [!Note]  
> <span data-ttu-id="58bee-106">Cette classe s’applique uniquement aux ordinateurs virtuels de génération 1.</span><span class="sxs-lookup"><span data-stu-id="58bee-106">This class only applies to generation 1 virtual machines.</span></span>

 

<span data-ttu-id="58bee-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="58bee-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58bee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58bee-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
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
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="58bee-109">Membres</span><span class="sxs-lookup"><span data-stu-id="58bee-109">Members</span></span>

<span data-ttu-id="58bee-110">La classe **MSVM \_ S3DisplayController** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="58bee-110">The **Msvm\_S3DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="58bee-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="58bee-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="58bee-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58bee-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="58bee-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="58bee-113">Methods</span></span>

<span data-ttu-id="58bee-114">La classe **MSVM \_ S3DisplayController** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="58bee-114">The **Msvm\_S3DisplayController** class has these methods.</span></span>



| <span data-ttu-id="58bee-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="58bee-115">Method</span></span>                                                                    | <span data-ttu-id="58bee-116">Description</span><span class="sxs-lookup"><span data-stu-id="58bee-116">Description</span></span>                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="58bee-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="58bee-117">**EnableDevice**</span></span>                                                          | <span data-ttu-id="58bee-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58bee-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="58bee-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="58bee-119">**OnlineDevice**</span></span>                                                          | <span data-ttu-id="58bee-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58bee-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="58bee-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="58bee-121">**QuiesceDevice**</span></span>                                                         | <span data-ttu-id="58bee-122">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58bee-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="58bee-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="58bee-123">**RequestStateChange**</span></span>](msvm-s3displaycontroller-requeststatechange.md) | <span data-ttu-id="58bee-124">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="58bee-124">Requests a state change.</span></span> <br/>     |
| [<span data-ttu-id="58bee-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="58bee-125">**Reset**</span></span>](msvm-s3displaycontroller-reset.md)                           | <span data-ttu-id="58bee-126">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="58bee-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="58bee-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="58bee-127">**RestoreProperties**</span></span>                                                     | <span data-ttu-id="58bee-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58bee-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="58bee-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="58bee-129">**SaveProperties**</span></span>                                                        | <span data-ttu-id="58bee-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58bee-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="58bee-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="58bee-131">**SetPowerState**</span></span>                                                         | <span data-ttu-id="58bee-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="58bee-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="58bee-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58bee-133">Properties</span></span>

<span data-ttu-id="58bee-134">La classe **MSVM \_ S3DisplayController** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="58bee-134">The **Msvm\_S3DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58bee-135">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="58bee-135">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-136">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-138">Les fonctionnalités graphiques et 3D du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="58bee-138">The graphics and 3D capabilities of the display controller.</span></span> <span data-ttu-id="58bee-139">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-139">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="58bee-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-141">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-143">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="58bee-143">Any additional availability and status of the device.</span></span> <span data-ttu-id="58bee-144">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="58bee-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-145">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="58bee-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-146">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-148">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="58bee-148">The primary availability and status of the device.</span></span> <span data-ttu-id="58bee-149">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="58bee-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="58bee-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bee-150">Value</span></span>                                                                        | <span data-ttu-id="58bee-151">Signification</span><span class="sxs-lookup"><span data-stu-id="58bee-151">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="58bee-152"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-152"><dt>6</dt></span></span> </dl> | <span data-ttu-id="58bee-153">Non applicable</span><span class="sxs-lookup"><span data-stu-id="58bee-153">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58bee-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="58bee-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-155">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-157">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="58bee-157">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="58bee-158">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="58bee-158">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-159">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="58bee-159">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-160">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="58bee-160">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-162">Tableau de chaînes de forme libre qui fournissent des explications plus détaillées sur les fonctionnalités de l’accélérateur vidéo indiquées dans le tableau **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="58bee-162">An array of free-form strings that provide more detailed explanations for any of the video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="58bee-163">Chaque entrée de ce tableau est liée à l’entrée dans le tableau **AcceleratorCapabilities** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="58bee-163">Each entry of this array is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span> <span data-ttu-id="58bee-164">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-164">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="58bee-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-168">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="58bee-168">A short description of the object.</span></span> <span data-ttu-id="58bee-169">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-170">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="58bee-170">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-171">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-173">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="58bee-173">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="58bee-174">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="58bee-174">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="58bee-175">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-175">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="58bee-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="58bee-176"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="58bee-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="58bee-178"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="58bee-179"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="58bee-180"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="58bee-181"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="58bee-182"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="58bee-183">)</span><span class="sxs-lookup"><span data-stu-id="58bee-183">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58bee-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="58bee-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-185">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-187">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="58bee-187">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="58bee-188">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur « MSVM \_ S3DisplayController ».</span><span class="sxs-lookup"><span data-stu-id="58bee-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_S3DisplayController".</span></span>

</dd> <dt>

<span data-ttu-id="58bee-189">**Description**</span><span class="sxs-lookup"><span data-stu-id="58bee-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-192">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="58bee-192">A description of the object.</span></span> <span data-ttu-id="58bee-193">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="58bee-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-195">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-197">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="58bee-197">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="58bee-198">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="58bee-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="58bee-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="58bee-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="58bee-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="58bee-201"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="58bee-202"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="58bee-203"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="58bee-204"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="58bee-205"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="58bee-206"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="58bee-207"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="58bee-208">)</span><span class="sxs-lookup"><span data-stu-id="58bee-208">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58bee-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="58bee-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-212">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="58bee-212">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="58bee-213">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="58bee-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="58bee-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-215">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-217">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="58bee-217">A display name for the object.</span></span> <span data-ttu-id="58bee-218">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-219">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="58bee-219">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-220">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-222">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="58bee-222">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="58bee-223">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="58bee-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bee-224">Value</span></span>                                                                        | <span data-ttu-id="58bee-225">Signification</span><span class="sxs-lookup"><span data-stu-id="58bee-225">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="58bee-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="58bee-227">activé</span><span class="sxs-lookup"><span data-stu-id="58bee-227">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="58bee-228"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-228"><dt>3</dt></span></span> </dl> | <span data-ttu-id="58bee-229">Désactivé</span><span class="sxs-lookup"><span data-stu-id="58bee-229">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58bee-230">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="58bee-230">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-233">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="58bee-233">The enabled and disabled states of an element.</span></span> <span data-ttu-id="58bee-234">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="58bee-234">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="58bee-235">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé) ou 3 (désactivée).</span><span class="sxs-lookup"><span data-stu-id="58bee-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="58bee-236">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bee-236">Value</span></span>                                                                        | <span data-ttu-id="58bee-237">Signification</span><span class="sxs-lookup"><span data-stu-id="58bee-237">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="58bee-238"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-238"><dt>2</dt></span></span> </dl> | <span data-ttu-id="58bee-239">activé</span><span class="sxs-lookup"><span data-stu-id="58bee-239">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="58bee-240"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-240"><dt>3</dt></span></span> </dl> | <span data-ttu-id="58bee-241">Désactivé</span><span class="sxs-lookup"><span data-stu-id="58bee-241">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58bee-242">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="58bee-242">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-243">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="58bee-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-245">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="58bee-245">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="58bee-246">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-247">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="58bee-247">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-248">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-249">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-250">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="58bee-250">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="58bee-251">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="58bee-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-253">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-255">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="58bee-255">The current health of the element.</span></span> <span data-ttu-id="58bee-256">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="58bee-256">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="58bee-257">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="58bee-257">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="58bee-258">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="58bee-259">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bee-259">Value</span></span>                                                                        | <span data-ttu-id="58bee-260">Signification</span><span class="sxs-lookup"><span data-stu-id="58bee-260">Meaning</span></span>       |
|------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="58bee-261"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-261"><dt>5</dt></span></span> </dl> | <span data-ttu-id="58bee-262">Ok</span><span class="sxs-lookup"><span data-stu-id="58bee-262">OK</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58bee-263">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="58bee-263">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-264">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="58bee-264">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-266">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="58bee-266">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="58bee-267">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="58bee-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="58bee-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-269">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="58bee-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-271">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="58bee-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="58bee-272">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="58bee-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58bee-276">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="58bee-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="58bee-277">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="58bee-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="58bee-278">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-279">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="58bee-279">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-280">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58bee-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-281">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-282">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="58bee-282">The last error code reported by the logical device.</span></span> <span data-ttu-id="58bee-283">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-283">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-284">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="58bee-284">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-285">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58bee-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-286">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-287">Quantité maximale de mémoire prise en charge, en octets.</span><span class="sxs-lookup"><span data-stu-id="58bee-287">The maximum amount of memory supported, in bytes.</span></span> <span data-ttu-id="58bee-288">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-288">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-289">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="58bee-289">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-290">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58bee-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-292">Nombre maximal d’entités directement adressables qui sont prises en charge par ce contrôleur.</span><span class="sxs-lookup"><span data-stu-id="58bee-292">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="58bee-293">La valeur 0 doit être utilisée si le nombre est inconnu ou illimité.</span><span class="sxs-lookup"><span data-stu-id="58bee-293">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="58bee-294">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="58bee-294">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="58bee-295">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="58bee-295">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-296">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="58bee-296">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-297">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58bee-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-299">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="58bee-299">This property has been deprecated.</span></span> <span data-ttu-id="58bee-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="58bee-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-301">**Nom**</span><span class="sxs-lookup"><span data-stu-id="58bee-301">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-302">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-304">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="58bee-304">The label by which the object is known.</span></span> <span data-ttu-id="58bee-305">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-306">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="58bee-306">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-307">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58bee-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-309">Nombre de pages vidéo prises en charge en fonction des résolutions actuelles et de la mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="58bee-309">The number of video pages supported given the current resolutions and available memory.</span></span> <span data-ttu-id="58bee-310">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-310">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-311">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="58bee-311">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-312">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-312">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-314">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="58bee-314">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="58bee-315">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="58bee-315">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="58bee-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="58bee-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="58bee-317"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="58bee-318"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="58bee-319"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="58bee-320"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="58bee-321"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="58bee-322"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="58bee-323"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="58bee-324"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="58bee-325"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="58bee-326"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="58bee-327"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="58bee-328"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="58bee-329"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="58bee-330"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="58bee-331"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="58bee-332"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="58bee-333"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="58bee-334"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="58bee-335"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="58bee-336">)</span><span class="sxs-lookup"><span data-stu-id="58bee-336">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58bee-337">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="58bee-337">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-338">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-340">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="58bee-340">The current statuses of the object.</span></span> <span data-ttu-id="58bee-341">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="58bee-341">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-342">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="58bee-342">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-345">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="58bee-345">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="58bee-346">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="58bee-346">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="58bee-347">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="58bee-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="58bee-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-349">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="58bee-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-351">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="58bee-351">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="58bee-352">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="58bee-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-353">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="58bee-353">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-354">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-356">Chaîne qui décrit le type d’architecture vidéo lorsque la propriété **VideoArchitecture** est 1 (« other »).</span><span class="sxs-lookup"><span data-stu-id="58bee-356">A string that describes the video architecture type when the **VideoArchitecture** property is 1 ("Other").</span></span> <span data-ttu-id="58bee-357">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-357">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-358">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="58bee-358">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-359">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-361">Type de mémoire vidéo lorsque la propriété **VideoMemoryType** de l’instance est 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="58bee-361">The video memory type when the instance's **VideoMemoryType** property is 1 (Other).</span></span> <span data-ttu-id="58bee-362">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-362">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-363">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="58bee-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-364">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-366">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="58bee-366">The power management capabilities of the device.</span></span> <span data-ttu-id="58bee-367">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-368">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="58bee-368">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-369">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="58bee-369">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-371">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="58bee-371">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="58bee-372">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-373">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="58bee-373">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-374">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58bee-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-375">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-376">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="58bee-376">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="58bee-377">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-377">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-378">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="58bee-378">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-379">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-380">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-381">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="58bee-381">Provides high level status information.</span></span> <span data-ttu-id="58bee-382">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="58bee-382">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="58bee-383">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="58bee-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="58bee-384">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="58bee-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="58bee-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="58bee-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="58bee-386"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="58bee-387"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="58bee-388"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="58bee-389"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="58bee-390"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="58bee-391">)</span><span class="sxs-lookup"><span data-stu-id="58bee-391">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58bee-392">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="58bee-392">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-393">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-395">Chaîne qui fournit des informations supplémentaires relatives au protocole pris en charge par le contrôleur.</span><span class="sxs-lookup"><span data-stu-id="58bee-395">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="58bee-396">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="58bee-396">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-397">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="58bee-397">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-398">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-399">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-400">Protocole utilisé par le contrôleur pour accéder aux appareils contrôlés.</span><span class="sxs-lookup"><span data-stu-id="58bee-400">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="58bee-401">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="58bee-401">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-402">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="58bee-402">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-403">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-405">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="58bee-405">The last requested or desired state for the element.</span></span> <span data-ttu-id="58bee-406">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="58bee-406">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="58bee-407">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="58bee-407">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="58bee-408">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-408">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="58bee-409">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bee-409">Value</span></span>                                                                         | <span data-ttu-id="58bee-410">Signification</span><span class="sxs-lookup"><span data-stu-id="58bee-410">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="58bee-411"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-411"><dt>12</dt></span></span> </dl> | <span data-ttu-id="58bee-412">Non applicable</span><span class="sxs-lookup"><span data-stu-id="58bee-412">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="58bee-413">**État**</span><span class="sxs-lookup"><span data-stu-id="58bee-413">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-414">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-416">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="58bee-416">The current status of the object.</span></span> <span data-ttu-id="58bee-417">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-418">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="58bee-418">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-419">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="58bee-419">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="58bee-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-421">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="58bee-421">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="58bee-422">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="58bee-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="58bee-423">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="58bee-423">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-424">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-425">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-426">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="58bee-426">The current state of the logical device.</span></span> <span data-ttu-id="58bee-427">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-428">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="58bee-428">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-429">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-431">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="58bee-431">The scoping system's creation class name.</span></span> <span data-ttu-id="58bee-432">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="58bee-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="58bee-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-435">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-436">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="58bee-436">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="58bee-437">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="58bee-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-438">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="58bee-438">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-439">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="58bee-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-441">La dernière fois que la machine virtuelle a été mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="58bee-441">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="58bee-442">Cette propriété est héritée [**du \_ contrôleur CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="58bee-442">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-443">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="58bee-443">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-444">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="58bee-444">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-446">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="58bee-446">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="58bee-447">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-447">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-448">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="58bee-448">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-449">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58bee-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-451">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="58bee-451">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="58bee-452">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="58bee-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-453">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="58bee-453">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-456">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="58bee-456">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="58bee-457">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="58bee-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="58bee-458">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="58bee-458">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-459">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-461">Spécifie l’architecture vidéo du contrôleur d’affichage utilisée pour générer le signal vidéo.</span><span class="sxs-lookup"><span data-stu-id="58bee-461">Specifies the display controller's video architecture used to generate the video signal.</span></span> <span data-ttu-id="58bee-462">En règle générale, un processeur vidéo dédié génère le signal vidéo conformément à l’architecture spécifiée.</span><span class="sxs-lookup"><span data-stu-id="58bee-462">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="58bee-463">Il s’agit d’un indicateur de la capacité de résolution maximale du contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="58bee-463">It is an indicator of the maximum resolution capability of the display controller.</span></span> <span data-ttu-id="58bee-464">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-464">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="58bee-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="58bee-465"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="58bee-466"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="58bee-467"><span id="CGA"></span><span id="cga"></span>**CGA** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="58bee-468"><span id="EGA"></span><span id="ega"></span>**EGA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="58bee-469"><span id="VGA"></span><span id="vga"></span>**VGA** (4)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="58bee-470"><span id="SVGA"></span><span id="svga"></span>**SVGA** (5)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="58bee-471"><span id="MDA"></span><span id="mda"></span>**MDA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="58bee-472"><span id="HGC"></span><span id="hgc"></span>**HGC** (7)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="58bee-473"><span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="58bee-474"><span id="8514A"></span><span id="8514a"></span>**8514A** (9)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="58bee-475"><span id="XGA"></span><span id="xga"></span>**XGA** (10)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Mémoire tampon de trame linéaire** (11)</span><span class="sxs-lookup"><span data-stu-id="58bee-476"><span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Linear Frame Buffer** (11)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="58bee-477"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="58bee-478"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="58bee-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="58bee-479"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="58bee-480">)</span><span class="sxs-lookup"><span data-stu-id="58bee-480">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58bee-481">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="58bee-481">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-482">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="58bee-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-483">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-484">Type de mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="58bee-484">The type of video memory.</span></span> <span data-ttu-id="58bee-485">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-485">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="58bee-486">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="58bee-486">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58bee-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="58bee-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58bee-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58bee-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58bee-489">Chaîne qui décrit le processeur/contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="58bee-489">A string that describes the video processor/controller.</span></span> <span data-ttu-id="58bee-490">Cette propriété est héritée de la [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58bee-490">This property is inherited from [**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58bee-491">Notes</span><span class="sxs-lookup"><span data-stu-id="58bee-491">Remarks</span></span>

<span data-ttu-id="58bee-492">L’accès à la classe **MSVM \_ S3DisplayController** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="58bee-492">Access to the **Msvm\_S3DisplayController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="58bee-493">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="58bee-493">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="58bee-494">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58bee-494">Requirements</span></span>



| <span data-ttu-id="58bee-495">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58bee-495">Requirement</span></span> | <span data-ttu-id="58bee-496">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bee-496">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58bee-497">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58bee-497">Minimum supported client</span></span><br/> | <span data-ttu-id="58bee-498">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58bee-498">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58bee-499">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58bee-499">Minimum supported server</span></span><br/> | <span data-ttu-id="58bee-500">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58bee-500">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58bee-501">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="58bee-501">Namespace</span></span><br/>                | <span data-ttu-id="58bee-502">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="58bee-502">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58bee-503">MOF</span><span class="sxs-lookup"><span data-stu-id="58bee-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58bee-504"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-504"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58bee-505">DLL</span><span class="sxs-lookup"><span data-stu-id="58bee-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58bee-506"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58bee-506"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58bee-507">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58bee-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bee-508">**\_DISPLAYCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="58bee-508">**CIM\_DisplayController**</span></span>](cim-displaycontroller.md)
</dt> <dt>

<span data-ttu-id="58bee-509">[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58bee-509">[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="58bee-510">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="58bee-510">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

