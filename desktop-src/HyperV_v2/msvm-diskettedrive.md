---
description: Représente un lecteur de disquette à l’intérieur de la machine virtuelle.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Msvm_DisketteDrive, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757654"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="52808-103">MSVM \_ DisketteDrive, classe</span><span class="sxs-lookup"><span data-stu-id="52808-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="52808-104">Représente un lecteur de disquette à l’intérieur de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="52808-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="52808-105">Un lecteur de disquette peut être rempli avec un fichier représentant une disquette ou le lecteur peut être vide.</span><span class="sxs-lookup"><span data-stu-id="52808-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="52808-106">Le support physique n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-106">Physical media is not supported.</span></span> <span data-ttu-id="52808-107">Il y a exactement un lecteur de disquette par contrôleur de disquette et il n’est pas amovible.</span><span class="sxs-lookup"><span data-stu-id="52808-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="52808-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="52808-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52808-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52808-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
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
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="52808-110">Membres</span><span class="sxs-lookup"><span data-stu-id="52808-110">Members</span></span>

<span data-ttu-id="52808-111">La classe **MSVM \_ DisketteDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52808-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="52808-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="52808-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="52808-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52808-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="52808-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="52808-114">Methods</span></span>

<span data-ttu-id="52808-115">La classe **MSVM \_ DisketteDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="52808-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="52808-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="52808-116">Method</span></span>                                                              | <span data-ttu-id="52808-117">Description</span><span class="sxs-lookup"><span data-stu-id="52808-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="52808-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="52808-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="52808-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="52808-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="52808-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="52808-121">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="52808-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="52808-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="52808-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="52808-123">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="52808-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="52808-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="52808-125">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="52808-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="52808-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="52808-127">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="52808-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="52808-128">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="52808-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="52808-129">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="52808-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="52808-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="52808-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="52808-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="52808-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="52808-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="52808-133">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="52808-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="52808-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="52808-135">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="52808-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="52808-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52808-136">Properties</span></span>

<span data-ttu-id="52808-137">La classe **MSVM \_ DisketteDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="52808-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52808-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="52808-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-139">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-141">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="52808-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="52808-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="52808-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="52808-143">Value</span></span>                                                                        | <span data-ttu-id="52808-144">Signification</span><span class="sxs-lookup"><span data-stu-id="52808-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="52808-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="52808-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="52808-146">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="52808-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="52808-147">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="52808-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-150">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-150">The primary availability and status of the device.</span></span> <span data-ttu-id="52808-151">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="52808-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="52808-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="52808-152">Value</span></span>                                                                        | <span data-ttu-id="52808-153">Signification</span><span class="sxs-lookup"><span data-stu-id="52808-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="52808-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="52808-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="52808-155">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="52808-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="52808-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="52808-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-157">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-159">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="52808-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="52808-160">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="52808-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="52808-161">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="52808-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="52808-162">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="52808-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="52808-163">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="52808-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="52808-164">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="52808-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-165">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-167">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="52808-167">The capabilities of the media access device.</span></span> <span data-ttu-id="52808-168">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie avec les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="52808-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="52808-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="52808-169">Value</span></span>                                                                                | <span data-ttu-id="52808-170">Signification</span><span class="sxs-lookup"><span data-stu-id="52808-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52808-171"><dt>{3, 4, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="52808-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="52808-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="52808-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="52808-173">L’entrée correspondante dans **CapabilityDescriptions** est « accès aléatoire ».</span><span class="sxs-lookup"><span data-stu-id="52808-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="52808-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="52808-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="52808-175">L’entrée correspondante dans **CapabilityDescriptions** est « prend en charge l’écriture ».</span><span class="sxs-lookup"><span data-stu-id="52808-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="52808-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="52808-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="52808-177">L’entrée correspondante dans **CapabilityDescriptions** est « prend en charge les supports amovibles ».</span><span class="sxs-lookup"><span data-stu-id="52808-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="52808-178">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="52808-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-179">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="52808-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-181">Tableau de chaînes de forme libre qui fournit des explications détaillées sur l’accès aux fonctionnalités d’appareil indiquées dans le tableau de propriétés **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="52808-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="52808-182">Chaque entrée de ce tableau est liée à l’entrée dans le tableau des **fonctionnalités** , située dans le même index.</span><span class="sxs-lookup"><span data-stu-id="52808-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="52808-183">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="52808-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-187">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52808-187">A short description of the object.</span></span> <span data-ttu-id="52808-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="52808-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="52808-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-192">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="52808-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="52808-193">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="52808-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="52808-194">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="52808-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-195">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="52808-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-198">Chaîne qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="52808-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="52808-199">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="52808-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="52808-200">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="52808-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="52808-201">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="52808-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="52808-202">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="52808-203">« Non compressé »</span><span class="sxs-lookup"><span data-stu-id="52808-203">"Not Compressed"</span></span>

<span data-ttu-id="52808-204">Connue</span><span class="sxs-lookup"><span data-stu-id="52808-204">"Unknown"</span></span>

<span data-ttu-id="52808-205">Compact</span><span class="sxs-lookup"><span data-stu-id="52808-205">"Compressed"</span></span>

<span data-ttu-id="52808-206">« Non compressé »</span><span class="sxs-lookup"><span data-stu-id="52808-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="52808-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="52808-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-208">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-210">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="52808-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="52808-211">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="52808-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-212">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="52808-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-213">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-215">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="52808-216">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-217">**Description**</span><span class="sxs-lookup"><span data-stu-id="52808-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-218">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-220">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="52808-220">A description of the object.</span></span> <span data-ttu-id="52808-221">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="52808-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="52808-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-225">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="52808-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="52808-226">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="52808-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="52808-227">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="52808-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-228">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="52808-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-231">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*».</span><span class="sxs-lookup"><span data-stu-id="52808-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="52808-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="52808-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-233">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-235">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52808-235">A display name for the object.</span></span> <span data-ttu-id="52808-236">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="52808-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="52808-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-238">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-240">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="52808-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="52808-241">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="52808-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="52808-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="52808-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-245">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="52808-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="52808-246">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="52808-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="52808-247">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 5 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="52808-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="52808-248">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="52808-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-249">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="52808-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52808-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-251">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="52808-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="52808-252">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="52808-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-256">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="52808-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="52808-257">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-258">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="52808-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-259">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-260">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-261">Chaîne qui décrit les types de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="52808-262">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="52808-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-264">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-266">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="52808-266">The current health of the element.</span></span> <span data-ttu-id="52808-267">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="52808-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="52808-268">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="52808-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="52808-269">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="52808-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="52808-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="52808-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-271">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="52808-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-273">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="52808-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="52808-274">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="52808-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="52808-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52808-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-276">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52808-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52808-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-278">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="52808-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="52808-279">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="52808-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="52808-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52808-283">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="52808-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="52808-284">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="52808-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="52808-285">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="52808-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-286">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="52808-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-287">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52808-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52808-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-289">Date et heure du dernier nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="52808-290">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-291">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="52808-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-292">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52808-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52808-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-294">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="52808-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="52808-295">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-296">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="52808-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-297">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-299">Durée, en millisecondes, entre la charge et la possibilité de lire ou d’écrire un média.</span><span class="sxs-lookup"><span data-stu-id="52808-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="52808-300">Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque qui ne tourne pas vers le disque signalant qu’il est prêt pour la lecture/écriture (c’est-à-dire le disque tournant à des vitesses nominales).</span><span class="sxs-lookup"><span data-stu-id="52808-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="52808-301">Pour les lecteurs de bande, il s’agit de l’heure à partir d’un support injecté pour signaler qu’il est prêt pour une application.</span><span class="sxs-lookup"><span data-stu-id="52808-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="52808-302">Il s’agit généralement de la zone de robot de la bande.</span><span class="sxs-lookup"><span data-stu-id="52808-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="52808-303">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-304">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="52808-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-305">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-307">Durée, en millisecondes, à passer du premier emplacement sur le média à l’emplacement le plus éloigné par rapport au temps.</span><span class="sxs-lookup"><span data-stu-id="52808-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="52808-308">Pour un lecteur de disque, il s’agit de la recherche complète et du délai de rotation complète.</span><span class="sxs-lookup"><span data-stu-id="52808-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="52808-309">Pour les lecteurs de bande, il s’agit d’une recherche à partir du début de la bande jusqu’au point le plus éloigné physiquement.</span><span class="sxs-lookup"><span data-stu-id="52808-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="52808-310">(La fin d’une bande peut être à son point le plus éloigné physiquement, mais cela n’est pas nécessairement vrai.) Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-311">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="52808-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-312">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-314">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="52808-315">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-316">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="52808-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-317">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-318">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-319">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="52808-320">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="52808-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="52808-321">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-322">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="52808-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-323">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-325">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="52808-325">This property has been deprecated.</span></span> <span data-ttu-id="52808-326">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-327">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="52808-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-328">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-330">Unités maximales qui peuvent être utilisées avant le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="52808-331">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-332">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="52808-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-333">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="52808-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52808-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-335">**True** si le média est verrouillé dans l’appareil et ne peut pas être éjecté ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="52808-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="52808-336">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-337">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="52808-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-338">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-340">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="52808-341">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-342">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="52808-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-343">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-345">Pour un appareil qui prend en charge les supports amovibles, le nombre de fois que ces médias ont été montés pour le transfert de données ou pour nettoyer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="52808-346">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="52808-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="52808-347">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-348">**Nom**</span><span class="sxs-lookup"><span data-stu-id="52808-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-351">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="52808-351">The label by which the object is known.</span></span> <span data-ttu-id="52808-352">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="52808-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="52808-353">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="52808-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-354">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="52808-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52808-355">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-356">**True** si l’appareil d’accès aux médias doit être nettoyé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="52808-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="52808-357">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-358">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="52808-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-359">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52808-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52808-360">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-361">Nombre maximal de plusieurs médias individuels qui peuvent être pris en charge ou insérés.</span><span class="sxs-lookup"><span data-stu-id="52808-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="52808-362">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="52808-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-364">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-366">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="52808-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="52808-367">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="52808-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="52808-368">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="52808-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="52808-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-370">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-372">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52808-372">The current statuses of the object.</span></span> <span data-ttu-id="52808-373">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="52808-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="52808-374">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="52808-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-375">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-376">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-377">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="52808-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="52808-378">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="52808-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="52808-379">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="52808-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="52808-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="52808-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-381">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="52808-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-383">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="52808-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="52808-384">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="52808-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="52808-385">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="52808-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-386">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-388">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-388">The power management capabilities of the device.</span></span> <span data-ttu-id="52808-389">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-390">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="52808-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-391">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="52808-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52808-392">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-393">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="52808-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="52808-394">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-395">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="52808-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-396">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-398">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="52808-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="52808-399">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-400">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="52808-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-401">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-403">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="52808-403">Provides high level status information.</span></span> <span data-ttu-id="52808-404">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="52808-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="52808-405">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="52808-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="52808-406">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="52808-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="52808-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="52808-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-408">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-410">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="52808-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="52808-411">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="52808-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="52808-412">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="52808-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="52808-413">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="52808-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="52808-414">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="52808-415">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="52808-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="52808-416">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="52808-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-417">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-419">La sécurité opérationnelle définie pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-419">The operational security defined for the device.</span></span> <span data-ttu-id="52808-420">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="52808-421">Valeur</span><span class="sxs-lookup"><span data-stu-id="52808-421">Value</span></span>                                                                        | <span data-ttu-id="52808-422">Signification</span><span class="sxs-lookup"><span data-stu-id="52808-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="52808-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="52808-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="52808-424">Aucun</span><span class="sxs-lookup"><span data-stu-id="52808-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="52808-425">**État**</span><span class="sxs-lookup"><span data-stu-id="52808-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-426">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-427">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-428">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="52808-428">The current status of the object.</span></span> <span data-ttu-id="52808-429">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-430">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="52808-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-431">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="52808-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="52808-432">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-433">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="52808-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="52808-434">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="52808-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="52808-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="52808-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-436">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-437">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-438">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="52808-438">The current state of the logical device.</span></span> <span data-ttu-id="52808-439">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-440">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="52808-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-441">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-442">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-443">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="52808-443">The scoping system's creation class name.</span></span> <span data-ttu-id="52808-444">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="52808-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="52808-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-446">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-447">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-448">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="52808-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="52808-449">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="52808-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-450">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="52808-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-451">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52808-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52808-452">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-453">Pour un appareil qui prend en charge les supports amovibles, la date et l’heure les plus récentes de montage du média sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="52808-454">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’a aucune signification et n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="52808-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="52808-455">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-456">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="52808-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-457">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52808-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52808-458">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-459">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="52808-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="52808-460">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="52808-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="52808-461">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="52808-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-462">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-463">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-464">Pour un appareil qui prend en charge les supports amovibles, durée totale (en secondes) de montage des médias pour le transfert de données ou le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="52808-465">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="52808-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="52808-466">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-467">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="52808-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-468">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-470">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="52808-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="52808-471">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-472">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="52808-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-473">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52808-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52808-474">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-475">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="52808-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="52808-476">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="52808-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="52808-477">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="52808-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-478">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52808-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52808-479">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-480">Taux de transfert de données soutenu, en Ko/s, que l’appareil peut lire et écrire sur un média.</span><span class="sxs-lookup"><span data-stu-id="52808-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="52808-481">Il s’agit d’un débit de données brutes soutenu.</span><span class="sxs-lookup"><span data-stu-id="52808-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="52808-482">Les taux ou taux maximaux en supposant que la compression ne doit pas être signalée dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="52808-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="52808-483">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-484">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="52808-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-485">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52808-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52808-486">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-487">Unités relatives à son utilisation dans **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="52808-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="52808-488">Cette propriété est héritée de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="52808-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="52808-489">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="52808-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-490">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-491">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-492">Nombre actuel d’unités utilisées.</span><span class="sxs-lookup"><span data-stu-id="52808-492">The current number of units used.</span></span> <span data-ttu-id="52808-493">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="52808-494">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="52808-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52808-495">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52808-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52808-496">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52808-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52808-497">Durée, en millisecondes, de la possibilité de lire ou d’écrire un média dans son « déchargement ».</span><span class="sxs-lookup"><span data-stu-id="52808-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="52808-498">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="52808-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52808-499">Notes</span><span class="sxs-lookup"><span data-stu-id="52808-499">Remarks</span></span>

<span data-ttu-id="52808-500">L’accès à la classe **MSVM \_ DisketteDrive** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="52808-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="52808-501">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="52808-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="52808-502">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52808-502">Requirements</span></span>



| <span data-ttu-id="52808-503">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52808-503">Requirement</span></span> | <span data-ttu-id="52808-504">Valeur</span><span class="sxs-lookup"><span data-stu-id="52808-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52808-505">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52808-505">Minimum supported client</span></span><br/> | <span data-ttu-id="52808-506">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52808-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="52808-507">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52808-507">Minimum supported server</span></span><br/> | <span data-ttu-id="52808-508">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52808-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52808-509">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52808-509">Namespace</span></span><br/>                | <span data-ttu-id="52808-510">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="52808-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="52808-511">MOF</span><span class="sxs-lookup"><span data-stu-id="52808-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52808-512"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52808-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52808-513">DLL</span><span class="sxs-lookup"><span data-stu-id="52808-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52808-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52808-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="52808-515">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52808-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52808-516">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="52808-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="52808-517">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="52808-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="52808-518">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="52808-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

