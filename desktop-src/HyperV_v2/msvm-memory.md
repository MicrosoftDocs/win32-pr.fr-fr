---
description: Représente la mémoire actuellement allouée à un ordinateur virtuel.
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Msvm_Memory, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868510"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="44de1-103">\_Classe de mémoire MSVM</span><span class="sxs-lookup"><span data-stu-id="44de1-103">Msvm\_Memory class</span></span>

<span data-ttu-id="44de1-104">Représente la mémoire actuellement allouée à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="44de1-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="44de1-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="44de1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="44de1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44de1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
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
  uint16   CreationClassName;
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="44de1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="44de1-107">Members</span></span>

<span data-ttu-id="44de1-108">La classe de **\_ mémoire MSVM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="44de1-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="44de1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="44de1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="44de1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="44de1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="44de1-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="44de1-111">Methods</span></span>

<span data-ttu-id="44de1-112">La classe de **\_ mémoire MSVM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="44de1-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="44de1-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="44de1-113">Method</span></span>                                                       | <span data-ttu-id="44de1-114">Description</span><span class="sxs-lookup"><span data-stu-id="44de1-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="44de1-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="44de1-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="44de1-116">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44de1-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="44de1-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="44de1-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="44de1-118">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44de1-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="44de1-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="44de1-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="44de1-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44de1-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="44de1-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="44de1-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="44de1-122">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="44de1-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="44de1-123">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="44de1-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="44de1-124">Réinitialise la mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="44de1-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="44de1-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="44de1-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="44de1-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44de1-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="44de1-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="44de1-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="44de1-128">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44de1-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="44de1-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="44de1-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="44de1-130">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="44de1-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="44de1-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="44de1-131">Properties</span></span>

<span data-ttu-id="44de1-132">La classe de **\_ mémoire MSVM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="44de1-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44de1-133">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="44de1-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-136">Décrit les propriétés en lecture/écriture du média.</span><span class="sxs-lookup"><span data-stu-id="44de1-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="44de1-137">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est définie sur 3 (lecture/écriture prise en charge) par défaut.</span><span class="sxs-lookup"><span data-stu-id="44de1-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="44de1-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-139">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-141">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="44de1-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="44de1-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-143">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="44de1-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-145">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-146">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="44de1-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-147">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-149">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="44de1-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-150">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="44de1-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-151">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-153">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="44de1-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="44de1-154">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44de1-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="44de1-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-156">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-158">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="44de1-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="44de1-159">Si vous spécifiez une taille de bloc variable, la taille maximale du bloc, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="44de1-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="44de1-160">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), entrez 1 (un).</span><span class="sxs-lookup"><span data-stu-id="44de1-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="44de1-161">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 1048576.</span><span class="sxs-lookup"><span data-stu-id="44de1-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="44de1-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-165">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="44de1-165">A short description of the object.</span></span> <span data-ttu-id="44de1-166">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="44de1-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-168">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-170">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="44de1-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="44de1-171">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="44de1-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="44de1-172">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="44de1-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="44de1-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="44de1-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="44de1-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="44de1-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="44de1-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="44de1-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="44de1-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="44de1-180">)</span><span class="sxs-lookup"><span data-stu-id="44de1-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="44de1-181">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="44de1-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-182">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-184">Nombre maximal de blocs, de tailles de **bloc**, qui sont disponibles pour la consommation lors de la superposition des extensions de stockage à l’aide de l’Association BasedOn.</span><span class="sxs-lookup"><span data-stu-id="44de1-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="44de1-185">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-186">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="44de1-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-187">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-189">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="44de1-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-191">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-193">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="44de1-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="44de1-194">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="44de1-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-195">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="44de1-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-196">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-198">Type d’organisation de données utilisé.</span><span class="sxs-lookup"><span data-stu-id="44de1-198">The type of data organization used.</span></span> <span data-ttu-id="44de1-199">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 2.</span><span class="sxs-lookup"><span data-stu-id="44de1-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-200">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="44de1-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-201">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-203">Nombre total de copies de données qui sont actuellement conservées.</span><span class="sxs-lookup"><span data-stu-id="44de1-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="44de1-204">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="44de1-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-205">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="44de1-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-206">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="44de1-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-208">Valeur actuelle pour la réservation Delta.</span><span class="sxs-lookup"><span data-stu-id="44de1-208">The current value for delta reservation.</span></span> <span data-ttu-id="44de1-209">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="44de1-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-210">**Description**</span><span class="sxs-lookup"><span data-stu-id="44de1-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-211">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-212">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-213">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="44de1-213">A description of the object.</span></span> <span data-ttu-id="44de1-214">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="44de1-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-216">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-218">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="44de1-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="44de1-219">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="44de1-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="44de1-220">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="44de1-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="44de1-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="44de1-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="44de1-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="44de1-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="44de1-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="44de1-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="44de1-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="44de1-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="44de1-229">)</span><span class="sxs-lookup"><span data-stu-id="44de1-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="44de1-230">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="44de1-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-232">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-233">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="44de1-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="44de1-234">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="44de1-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="44de1-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-238">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="44de1-238">A display name for the object.</span></span> <span data-ttu-id="44de1-239">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="44de1-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-241">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-243">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="44de1-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="44de1-244">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44de1-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="44de1-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-246">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-248">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="44de1-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="44de1-249">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="44de1-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="44de1-250">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44de1-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="44de1-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="44de1-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="44de1-252">Signification</span><span class="sxs-lookup"><span data-stu-id="44de1-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="44de1-253"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="44de1-254">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="44de1-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="44de1-255"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="44de1-256"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="44de1-257">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="44de1-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="44de1-258"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="44de1-259">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="44de1-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="44de1-260"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="44de1-261">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="44de1-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="44de1-262"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="44de1-263">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="44de1-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="44de1-264"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="44de1-265">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="44de1-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="44de1-266"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="44de1-267">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="44de1-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="44de1-268"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="44de1-269">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="44de1-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="44de1-270"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="44de1-271">L’élément est activé, mais il est en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="44de1-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="44de1-272">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="44de1-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="44de1-273">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="44de1-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="44de1-274">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="44de1-275">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="44de1-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="44de1-276">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="44de1-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="44de1-277">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="44de1-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-278">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-280">Adresse de fin du bloc de mémoire contigu.</span><span class="sxs-lookup"><span data-stu-id="44de1-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="44de1-281">Étant donné que **la propriété de l’ordinateur de la** valeur est toujours 0, cette valeur reflète toujours la quantité totale de mémoire de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="44de1-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="44de1-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-285">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="44de1-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-287">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-289">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-290">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="44de1-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-291">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-293">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-294">**Partagefichiers**</span><span class="sxs-lookup"><span data-stu-id="44de1-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-295">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="44de1-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-297">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="44de1-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-299">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-301">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="44de1-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-305">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44de1-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-307">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-309">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-310">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="44de1-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-311">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-313">Chaîne qui décrit le type de détection d’erreurs et de correction pris en charge par cette extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="44de1-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="44de1-314">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="44de1-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-316">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-317">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-318">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="44de1-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-320">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44de1-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-322">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory) , mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="44de1-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-324">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44de1-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-326">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-327">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="44de1-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-328">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-330">Les extensions de stockage ont des informations d’État supplémentaires au-delà de celles capturées dans le **OperationalStatus** et d’autres propriétés héritées de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="44de1-331">Ces informations supplémentaires (par exemple, « protection désactivée », valeur = 9) sont capturées dans la propriété **VolumeStatus** .</span><span class="sxs-lookup"><span data-stu-id="44de1-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="44de1-332">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 2 (aucun/non applicable).</span><span class="sxs-lookup"><span data-stu-id="44de1-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="44de1-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-334">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-336">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="44de1-336">The current health of the element.</span></span> <span data-ttu-id="44de1-337">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="44de1-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="44de1-338">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="44de1-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="44de1-339">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="44de1-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="44de1-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-341">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="44de1-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-343">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="44de1-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-345">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44de1-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-347">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="44de1-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="44de1-348">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="44de1-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-350">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44de1-352">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="44de1-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="44de1-353">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="44de1-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="44de1-354">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-355">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="44de1-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-356">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-357">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-358">**True** si les extensions de stockage sous-jacentes participent à un groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="44de1-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="44de1-359">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="44de1-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="44de1-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-361">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44de1-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-363">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-364">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="44de1-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-365">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-367">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-368">**Nom**</span><span class="sxs-lookup"><span data-stu-id="44de1-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-369">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44de1-371">Qualificateurs : **MaxLen** (1024), **override** ("Name")</span><span class="sxs-lookup"><span data-stu-id="44de1-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="44de1-372">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="44de1-372">The label by which the object is known.</span></span> <span data-ttu-id="44de1-373">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="44de1-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="44de1-374">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur «*GUID*».</span><span class="sxs-lookup"><span data-stu-id="44de1-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="44de1-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="44de1-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-376">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-378">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="44de1-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-379">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="44de1-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-380">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-382">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="44de1-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-383">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="44de1-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-384">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-386">**True** s’il n’existe aucun point de défaillance unique.</span><span class="sxs-lookup"><span data-stu-id="44de1-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="44de1-387">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="44de1-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="44de1-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-389">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-391">Valeur calculée qui représente la quantité totale de mémoire divisée par la taille de **bloc**.</span><span class="sxs-lookup"><span data-stu-id="44de1-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="44de1-392">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="44de1-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-393">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="44de1-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-394">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-395">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-396">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="44de1-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="44de1-397">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="44de1-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="44de1-398">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="44de1-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="44de1-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="44de1-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="44de1-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="44de1-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="44de1-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="44de1-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="44de1-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="44de1-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="44de1-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="44de1-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="44de1-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="44de1-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="44de1-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="44de1-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="44de1-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="44de1-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="44de1-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="44de1-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="44de1-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="44de1-418">)</span><span class="sxs-lookup"><span data-stu-id="44de1-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="44de1-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="44de1-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-420">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-422">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="44de1-422">The current statuses of the object.</span></span> <span data-ttu-id="44de1-423">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-424">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="44de1-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-425">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-427">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="44de1-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="44de1-428">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="44de1-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="44de1-429">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-430">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="44de1-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-431">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-433">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="44de1-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-435">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="44de1-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-436">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-437">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-438">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="44de1-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-441">Espace de noms de la propriété **Name** lorsque la propriété **NameFormat** contient la valeur 1 (Other ").</span><span class="sxs-lookup"><span data-stu-id="44de1-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="44de1-442">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-443">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="44de1-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-444">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-446">Espace de noms de la propriété **Name** lorsque la propriété **NameNamespace** comprend la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="44de1-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="44de1-447">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="44de1-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-448">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="44de1-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-449">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-451">Nombre de packages physiques qui peuvent échouer actuellement sans perte de données.</span><span class="sxs-lookup"><span data-stu-id="44de1-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="44de1-452">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="44de1-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-453">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="44de1-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-454">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-456">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-457">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="44de1-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-458">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-460">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-461">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="44de1-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-462">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-463">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-464">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-465">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="44de1-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-466">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-467">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-468">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="44de1-468">Provides high level status information.</span></span> <span data-ttu-id="44de1-469">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="44de1-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="44de1-470">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="44de1-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="44de1-471">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="44de1-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="44de1-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="44de1-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="44de1-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="44de1-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="44de1-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="44de1-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="44de1-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="44de1-478">)</span><span class="sxs-lookup"><span data-stu-id="44de1-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="44de1-479">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="44de1-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-480">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-482">**True** si le système conteneur ne peut pas créer ou supprimer cet élément opérationnel.</span><span class="sxs-lookup"><span data-stu-id="44de1-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="44de1-483">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="44de1-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-484">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="44de1-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-485">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-487">Chaîne qui décrit le média et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="44de1-487">A string that describes the media and its use.</span></span> <span data-ttu-id="44de1-488">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur « mémoire système ».</span><span class="sxs-lookup"><span data-stu-id="44de1-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="44de1-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="44de1-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-490">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-491">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-492">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="44de1-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="44de1-493">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="44de1-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="44de1-494">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="44de1-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="44de1-495">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="44de1-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="44de1-496">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="44de1-497">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="44de1-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="44de1-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-499">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-501">**True** si le stockage est accessible de manière séquentielle par un périphérique d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="44de1-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="44de1-502">Une partition de bande est un exemple d’extension de stockage à accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="44de1-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="44de1-503">Les volumes de stockage, les partitions de disque et les disques logiques représentent des étendues ayant un accès aléatoire.</span><span class="sxs-lookup"><span data-stu-id="44de1-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="44de1-504">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est toujours définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="44de1-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-505">**De la**</span><span class="sxs-lookup"><span data-stu-id="44de1-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-506">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-508">Adresse de début référencée par une application ou un système d’exploitation et mappée par un contrôleur de mémoire pour cet objet mémoire.</span><span class="sxs-lookup"><span data-stu-id="44de1-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="44de1-509">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory)et est toujours définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="44de1-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-510">**État**</span><span class="sxs-lookup"><span data-stu-id="44de1-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-512">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-513">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-514">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="44de1-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-515">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="44de1-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="44de1-516">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-517">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="44de1-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="44de1-518">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="44de1-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="44de1-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-520">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-521">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-522">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-523">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="44de1-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-524">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-525">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-526">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="44de1-526">The scoping system's creation class name.</span></span> <span data-ttu-id="44de1-527">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="44de1-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="44de1-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-529">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-531">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="44de1-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-533">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="44de1-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-534">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-535">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="44de1-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="44de1-536">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="44de1-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-537">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="44de1-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-538">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44de1-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-539">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-540">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="44de1-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="44de1-541">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur « null ».</span><span class="sxs-lookup"><span data-stu-id="44de1-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="44de1-542">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="44de1-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-543">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44de1-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-544">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-545">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="44de1-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44de1-546">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="44de1-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-547">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44de1-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-548">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-549">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="44de1-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="44de1-550">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44de1-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="44de1-551">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="44de1-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44de1-552">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="44de1-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44de1-553">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="44de1-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44de1-554">Indique si la mémoire est volatile.</span><span class="sxs-lookup"><span data-stu-id="44de1-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="44de1-555">Cette propriété est héritée de la [**\_ mémoire CIM**](/windows/desktop/CIMWin32Prov/cim-memory)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="44de1-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44de1-556">Notes</span><span class="sxs-lookup"><span data-stu-id="44de1-556">Remarks</span></span>

<span data-ttu-id="44de1-557">L’accès à la classe de **\_ mémoire MSVM** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="44de1-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="44de1-558">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="44de1-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="44de1-559">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44de1-559">Requirements</span></span>



| <span data-ttu-id="44de1-560">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44de1-560">Requirement</span></span> | <span data-ttu-id="44de1-561">Valeur</span><span class="sxs-lookup"><span data-stu-id="44de1-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44de1-562">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44de1-562">Minimum supported client</span></span><br/> | <span data-ttu-id="44de1-563">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44de1-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="44de1-564">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44de1-564">Minimum supported server</span></span><br/> | <span data-ttu-id="44de1-565">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44de1-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44de1-566">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="44de1-566">Namespace</span></span><br/>                | <span data-ttu-id="44de1-567">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="44de1-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="44de1-568">MOF</span><span class="sxs-lookup"><span data-stu-id="44de1-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44de1-569"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44de1-570">DLL</span><span class="sxs-lookup"><span data-stu-id="44de1-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44de1-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44de1-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44de1-572">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44de1-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44de1-573">**\_Mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="44de1-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="44de1-574">**\_Mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="44de1-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="44de1-575">Classes de mémoire</span><span class="sxs-lookup"><span data-stu-id="44de1-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

