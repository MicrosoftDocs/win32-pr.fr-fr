---
description: Représente un lecteur de disque dur à l’intérieur d’une machine virtuelle.
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Msvm_DiskDrive, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867958"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="d341b-103">MSVM \_ DiskDrive, classe</span><span class="sxs-lookup"><span data-stu-id="d341b-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="d341b-104">Représente un lecteur de disque dur à l’intérieur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d341b-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="d341b-105">Ce lecteur de disque dur peut être un périphérique direct (si un disque dur physique a été attaché à l’ordinateur virtuel) ou un périphérique synthétique qui est rempli avec un support de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d341b-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="d341b-106">Étant donné que des disques durs virtuels et physiques peuvent être ajoutés et supprimés de la machine virtuelle, il existe deux pools de ressources associés à cette classe, l’un pour les disques durs directs et l’autre pour les disques durs virtuels.</span><span class="sxs-lookup"><span data-stu-id="d341b-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="d341b-107">Les disques durs peuvent uniquement être ajoutés ou supprimés du contrôleur SCSI virtuel lorsque l’ordinateur virtuel est en ligne.</span><span class="sxs-lookup"><span data-stu-id="d341b-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="d341b-108">Les disques peuvent uniquement être ajoutés ou supprimés du contrôleur IDE virtuel lorsque l’ordinateur virtuel est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d341b-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="d341b-109">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d341b-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d341b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d341b-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="d341b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d341b-111">Members</span></span>

<span data-ttu-id="d341b-112">La classe **MSVM \_ DiskDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d341b-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="d341b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d341b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="d341b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d341b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d341b-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d341b-115">Methods</span></span>

<span data-ttu-id="d341b-116">La classe **MSVM \_ DiskDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d341b-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="d341b-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="d341b-117">Method</span></span>                                                          | <span data-ttu-id="d341b-118">Description</span><span class="sxs-lookup"><span data-stu-id="d341b-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="d341b-119">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="d341b-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="d341b-120">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d341b-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d341b-121">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="d341b-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="d341b-122">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="d341b-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="d341b-123">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="d341b-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="d341b-124">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d341b-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d341b-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="d341b-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="d341b-126">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d341b-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="d341b-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="d341b-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="d341b-128">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="d341b-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="d341b-129">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="d341b-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="d341b-130">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="d341b-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="d341b-131">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="d341b-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="d341b-132">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d341b-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d341b-133">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="d341b-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="d341b-134">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d341b-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="d341b-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d341b-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="d341b-136">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d341b-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d341b-137">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d341b-137">Properties</span></span>

<span data-ttu-id="d341b-138">La classe **MSVM \_ DiskDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d341b-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d341b-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="d341b-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-140">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="d341b-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-143">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="d341b-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-146">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d341b-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="d341b-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-148">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-150">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d341b-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="d341b-151">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d341b-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-152">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d341b-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-153">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-155">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="d341b-155">The capabilities of the media access device.</span></span> <span data-ttu-id="d341b-156">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie avec les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d341b-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="d341b-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="d341b-157">Value</span></span>                                                                        | <span data-ttu-id="d341b-158">Signification</span><span class="sxs-lookup"><span data-stu-id="d341b-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d341b-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="d341b-160">L’entrée correspondante dans **CapabilityDescriptions** est « accès aléatoire ».</span><span class="sxs-lookup"><span data-stu-id="d341b-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="d341b-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="d341b-162">L’entrée correspondante dans **CapabilityDescriptions** est « prend en charge l’écriture ».</span><span class="sxs-lookup"><span data-stu-id="d341b-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d341b-163">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d341b-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-164">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d341b-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-166">Tableau de chaînes de forme libre qui fournit des explications détaillées sur l’accès aux fonctionnalités d’appareil indiquées dans le tableau de propriétés **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d341b-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="d341b-167">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés des **fonctionnalités** , situé dans le même index.</span><span class="sxs-lookup"><span data-stu-id="d341b-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="d341b-168">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="d341b-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d341b-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-172">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d341b-172">A short description of the object.</span></span> <span data-ttu-id="d341b-173">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-174">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d341b-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-175">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-177">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d341b-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d341b-178">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d341b-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d341b-179">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d341b-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d341b-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d341b-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="d341b-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="d341b-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="d341b-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d341b-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d341b-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d341b-187">)</span><span class="sxs-lookup"><span data-stu-id="d341b-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d341b-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="d341b-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-191">Chaîne qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="d341b-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="d341b-192">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="d341b-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="d341b-193">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="d341b-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="d341b-194">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="d341b-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="d341b-195">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="d341b-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="d341b-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d341b-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-197">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-199">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="d341b-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d341b-200">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d341b-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-201">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d341b-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-202">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-204">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="d341b-205">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 512.</span><span class="sxs-lookup"><span data-stu-id="d341b-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-206">**Description**</span><span class="sxs-lookup"><span data-stu-id="d341b-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-209">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="d341b-209">A description of the object.</span></span> <span data-ttu-id="d341b-210">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d341b-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-212">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-214">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d341b-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d341b-215">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d341b-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d341b-216">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d341b-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="d341b-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="d341b-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="d341b-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="d341b-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="d341b-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="d341b-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d341b-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d341b-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d341b-225">)</span><span class="sxs-lookup"><span data-stu-id="d341b-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d341b-226">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d341b-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-229">Une adresse ou d’autres informations d’identification pour nommer de façon unique l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="d341b-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="d341b-230">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d341b-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-231">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="d341b-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-232">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d341b-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-234">Le nombre de lecteurs physiques sur le système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="d341b-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d341b-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-236">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-238">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d341b-238">A display name for the object.</span></span> <span data-ttu-id="d341b-239">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="d341b-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-241">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-243">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d341b-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="d341b-244">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d341b-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="d341b-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-246">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-248">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="d341b-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="d341b-249">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="d341b-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="d341b-250">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d341b-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="d341b-251">Valeur</span><span class="sxs-lookup"><span data-stu-id="d341b-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="d341b-252">Signification</span><span class="sxs-lookup"><span data-stu-id="d341b-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="d341b-253"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="d341b-254">Impossible de déterminer l’état de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d341b-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="d341b-255"><dt>**Autre**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="d341b-256"><dt>**Activé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="d341b-257">L’élément est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d341b-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="d341b-258"><dt>**Désactivé**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="d341b-259">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d341b-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="d341b-260"><dt>**Arrêt**</dt> de <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="d341b-261">L’élément est en cours de passage à un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="d341b-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="d341b-262"><dt>**Non applicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="d341b-263">L’élément ne prend pas en charge l’activation ou la désactivation.</span><span class="sxs-lookup"><span data-stu-id="d341b-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="d341b-264"><dt>**Activé mais hors connexion**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="d341b-265">L’élément peut exécuter des commandes et supprimer toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="d341b-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="d341b-266"><dt>**Dans le test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="d341b-267">L’élément est dans un état de test.</span><span class="sxs-lookup"><span data-stu-id="d341b-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="d341b-268"><dt>**Différé**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="d341b-269">L’élément peut exécuter des commandes, mais il met en file d’attente toutes les nouvelles demandes.</span><span class="sxs-lookup"><span data-stu-id="d341b-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="d341b-270"><dt>**Suspension**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="d341b-271">L’élément est activé, mais il est en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="d341b-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="d341b-272">Le comportement de l’élément est similaire à l’état activé (2), mais ne traite qu’un ensemble restreint de commandes.</span><span class="sxs-lookup"><span data-stu-id="d341b-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="d341b-273">Toutes les autres demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d341b-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="d341b-274">À <dt>**partir**</dt> de <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="d341b-275">L’élément est en train d’accéder à un état activé (2).</span><span class="sxs-lookup"><span data-stu-id="d341b-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="d341b-276">Les nouvelles demandes sont mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d341b-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="d341b-277">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d341b-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-278">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d341b-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-279">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-280">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d341b-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-284">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-285">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="d341b-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-288">Chaîne qui décrit les types de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="d341b-289">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur « None ».</span><span class="sxs-lookup"><span data-stu-id="d341b-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="d341b-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d341b-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-291">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-293">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d341b-293">The current health of the element.</span></span> <span data-ttu-id="d341b-294">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d341b-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d341b-295">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d341b-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d341b-296">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="d341b-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d341b-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-298">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d341b-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-300">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d341b-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-302">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-303">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-304">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="d341b-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d341b-305">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d341b-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d341b-309">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="d341b-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d341b-310">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="d341b-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d341b-311">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-312">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="d341b-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-313">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-315">Date et heure du dernier nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="d341b-316">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d341b-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-318">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d341b-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-320">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-321">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-322">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-323">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-324">Durée, en millisecondes, entre la charge et la possibilité de lire ou d’écrire un média.</span><span class="sxs-lookup"><span data-stu-id="d341b-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="d341b-325">Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque qui ne tourne pas vers le disque signalant qu’il est prêt pour la lecture/écriture (c’est-à-dire le disque tournant à des vitesses nominales).</span><span class="sxs-lookup"><span data-stu-id="d341b-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="d341b-326">Pour les lecteurs de bande, il s’agit de l’heure à partir d’un support injecté pour signaler qu’il est prêt pour une application.</span><span class="sxs-lookup"><span data-stu-id="d341b-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="d341b-327">Il s’agit généralement de la zone de robot de la bande.</span><span class="sxs-lookup"><span data-stu-id="d341b-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="d341b-328">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) et est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-329">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-330">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-332">Durée, en millisecondes, à passer du premier emplacement sur le média à l’emplacement le plus éloigné par rapport au temps.</span><span class="sxs-lookup"><span data-stu-id="d341b-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="d341b-333">Pour un lecteur de disque, cela représente une recherche complète et un délai de rotation totale.</span><span class="sxs-lookup"><span data-stu-id="d341b-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="d341b-334">Pour les lecteurs de bande, il s’agit d’une recherche à partir du début de la bande jusqu’au point le plus éloigné physiquement.</span><span class="sxs-lookup"><span data-stu-id="d341b-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="d341b-335">(La fin d’une bande peut être à son point le plus éloigné physiquement, mais cela n’est pas nécessairement vrai.) Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-336">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d341b-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-337">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-339">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="d341b-340">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 512 pour les lecteurs de disque dur virtuel, variable pour les lecteurs directs.</span><span class="sxs-lookup"><span data-stu-id="d341b-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-341">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="d341b-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-342">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-344">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="d341b-345">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="d341b-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="d341b-346">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 2 milliards pour les lecteurs de disque dur virtuel, variable pour les lecteurs directs.</span><span class="sxs-lookup"><span data-stu-id="d341b-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-347">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-348">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-349">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-350">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-351">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="d341b-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-352">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-354">Unités maximales qui peuvent être utilisées avant le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="d341b-355">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d341b-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-356">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="d341b-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-357">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d341b-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-359">**True** si le média est verrouillé dans l’appareil et ne peut pas être éjecté ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d341b-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="d341b-360">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et a la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="d341b-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-361">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d341b-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-362">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-364">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="d341b-365">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 512.</span><span class="sxs-lookup"><span data-stu-id="d341b-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-366">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="d341b-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-367">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-368">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-369">Pour un appareil qui prend en charge les supports amovibles, le nombre de fois que ces médias ont été montés pour le transfert de données ou pour nettoyer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="d341b-370">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="d341b-371">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-372">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d341b-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-374">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-375">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="d341b-375">The label by which the object is known.</span></span> <span data-ttu-id="d341b-376">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-377">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="d341b-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-378">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d341b-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-380">**True** si l’appareil d’accès aux médias doit être nettoyé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d341b-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="d341b-381">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="d341b-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-382">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="d341b-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-383">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d341b-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-385">Nombre maximal de plusieurs médias individuels qui peuvent être pris en charge ou insérés.</span><span class="sxs-lookup"><span data-stu-id="d341b-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="d341b-386">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="d341b-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-387">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d341b-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-388">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-389">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-390">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d341b-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d341b-391">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d341b-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d341b-392">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d341b-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d341b-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="d341b-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="d341b-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="d341b-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="d341b-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="d341b-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="d341b-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="d341b-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="d341b-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="d341b-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="d341b-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="d341b-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="d341b-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="d341b-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="d341b-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="d341b-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="d341b-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d341b-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d341b-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d341b-412">)</span><span class="sxs-lookup"><span data-stu-id="d341b-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d341b-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d341b-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-414">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-415">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-416">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d341b-416">The current statuses of the object.</span></span> <span data-ttu-id="d341b-417">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-418">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="d341b-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-419">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-420">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-421">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="d341b-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="d341b-422">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="d341b-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="d341b-423">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d341b-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-425">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d341b-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-426">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-427">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-428">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d341b-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-429">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-430">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-431">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-432">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d341b-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-433">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d341b-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-434">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-435">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d341b-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-437">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-439">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-440">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d341b-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-441">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-443">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="d341b-443">Provides high level status information.</span></span> <span data-ttu-id="d341b-444">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="d341b-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d341b-445">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="d341b-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="d341b-446">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="d341b-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="d341b-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="d341b-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="d341b-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="d341b-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="d341b-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d341b-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="d341b-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="d341b-453">)</span><span class="sxs-lookup"><span data-stu-id="d341b-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d341b-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="d341b-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-455">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-456">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-457">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="d341b-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="d341b-458">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="d341b-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="d341b-459">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="d341b-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="d341b-460">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="d341b-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="d341b-461">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="d341b-462">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="d341b-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-463">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="d341b-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-464">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-466">La sécurité opérationnelle définie pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-466">The operational security defined for the device.</span></span> <span data-ttu-id="d341b-467">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 3 (aucune).</span><span class="sxs-lookup"><span data-stu-id="d341b-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-468">**État**</span><span class="sxs-lookup"><span data-stu-id="d341b-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-471">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-472">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d341b-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-473">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="d341b-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d341b-474">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-475">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d341b-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d341b-476">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d341b-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d341b-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-478">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-480">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-481">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d341b-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-482">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-483">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-484">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d341b-484">The scoping system's creation class name.</span></span> <span data-ttu-id="d341b-485">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d341b-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d341b-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-488">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-489">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d341b-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="d341b-490">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="d341b-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-491">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="d341b-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-492">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-493">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-494">Pour un appareil qui prend en charge les supports amovibles, la date et l’heure les plus récentes de montage du média sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="d341b-495">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’a aucune signification et n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="d341b-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="d341b-496">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-497">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="d341b-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-498">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-499">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-500">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="d341b-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="d341b-501">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur « null ».</span><span class="sxs-lookup"><span data-stu-id="d341b-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="d341b-502">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-503">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-505">Pour un appareil qui prend en charge les supports amovibles, durée totale (en secondes) de montage des médias pour le transfert de données ou le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d341b-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="d341b-506">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="d341b-507">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-508">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="d341b-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-509">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-510">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-511">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="d341b-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-512">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="d341b-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-513">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d341b-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-515">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="d341b-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="d341b-516">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d341b-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d341b-517">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="d341b-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-518">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d341b-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-519">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-520">Taux de transfert de données soutenu, en Ko/s, que l’appareil peut lire et écrire sur un média.</span><span class="sxs-lookup"><span data-stu-id="d341b-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="d341b-521">Il s’agit d’un débit de données brutes soutenu.</span><span class="sxs-lookup"><span data-stu-id="d341b-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="d341b-522">Les taux ou taux maximaux en supposant que la compression ne doit pas être signalée dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d341b-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="d341b-523">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-524">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="d341b-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-525">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d341b-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-526">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-527">Unités relatives à son utilisation dans **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="d341b-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="d341b-528">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="d341b-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-529">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="d341b-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-530">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-531">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-532">Nombre actuel d’unités utilisées.</span><span class="sxs-lookup"><span data-stu-id="d341b-532">The current number of units used.</span></span> <span data-ttu-id="d341b-533">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d341b-534">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="d341b-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d341b-535">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d341b-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d341b-536">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d341b-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d341b-537">Durée, en millisecondes, de la possibilité de lire ou d’écrire un support à son déchargement.</span><span class="sxs-lookup"><span data-stu-id="d341b-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="d341b-538">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="d341b-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d341b-539">Notes</span><span class="sxs-lookup"><span data-stu-id="d341b-539">Remarks</span></span>

<span data-ttu-id="d341b-540">L’accès à la classe **MSVM \_ DiskDrive** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="d341b-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d341b-541">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d341b-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d341b-542">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d341b-542">Requirements</span></span>



| <span data-ttu-id="d341b-543">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d341b-543">Requirement</span></span> | <span data-ttu-id="d341b-544">Valeur</span><span class="sxs-lookup"><span data-stu-id="d341b-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d341b-545">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d341b-545">Minimum supported client</span></span><br/> | <span data-ttu-id="d341b-546">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d341b-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d341b-547">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d341b-547">Minimum supported server</span></span><br/> | <span data-ttu-id="d341b-548">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d341b-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d341b-549">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d341b-549">Namespace</span></span><br/>                | <span data-ttu-id="d341b-550">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d341b-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d341b-551">MOF</span><span class="sxs-lookup"><span data-stu-id="d341b-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d341b-552"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d341b-553">DLL</span><span class="sxs-lookup"><span data-stu-id="d341b-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d341b-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d341b-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d341b-555">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d341b-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d341b-556">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="d341b-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="d341b-557">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="d341b-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="d341b-558">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="d341b-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

