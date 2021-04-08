---
description: Représente un lecteur de DVD à l’intérieur d’une machine virtuelle.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Msvm_DVDDrive, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867954"
---
# <a name="msvm_dvddrive-class"></a><span data-ttu-id="35dc1-103">MSVM \_ DVDDrive, classe</span><span class="sxs-lookup"><span data-stu-id="35dc1-103">Msvm\_DVDDrive class</span></span>

<span data-ttu-id="35dc1-104">Représente un lecteur de DVD à l’intérieur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="35dc1-104">Represents a DVD drive inside of a virtual machine.</span></span> <span data-ttu-id="35dc1-105">Ce lecteur de DVD peut être un périphérique direct (si un disque dur physique a été attaché à la machine virtuelle) ou synthétique et rempli avec un support de fichier ISO.</span><span class="sxs-lookup"><span data-stu-id="35dc1-105">This DVD drive can either be a pass-through device (if a physical hard disk was attached to the virtual machine) or synthetic and populated with ISO file media.</span></span> <span data-ttu-id="35dc1-106">Étant donné que les lecteurs de DVD virtuels et physiques peuvent être ajoutés et supprimés de la machine virtuelle, il existe deux pools de ressources associés à cette classe, l’un pour les lecteurs de DVD direct et l’autre pour les lecteurs de DVD virtuels.</span><span class="sxs-lookup"><span data-stu-id="35dc1-106">Because virtual and physical DVD drives can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through DVD drives, and the other for virtual DVD drives.</span></span> <span data-ttu-id="35dc1-107">Les lecteurs de DVD ne peuvent être ajoutés ou supprimés que si la machine virtuelle est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="35dc1-107">DVD drives can only be added or removed if the virtual machine is offline.</span></span>

<span data-ttu-id="35dc1-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="35dc1-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35dc1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35dc1-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
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
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a><span data-ttu-id="35dc1-110">Membres</span><span class="sxs-lookup"><span data-stu-id="35dc1-110">Members</span></span>

<span data-ttu-id="35dc1-111">La classe **MSVM \_ DVDDrive** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="35dc1-111">The **Msvm\_DVDDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="35dc1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35dc1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="35dc1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35dc1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="35dc1-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35dc1-114">Methods</span></span>

<span data-ttu-id="35dc1-115">La classe **MSVM \_ DVDDrive** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="35dc1-115">The **Msvm\_DVDDrive** class has these methods.</span></span>



| <span data-ttu-id="35dc1-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="35dc1-116">Method</span></span>                                                         | <span data-ttu-id="35dc1-117">Description</span><span class="sxs-lookup"><span data-stu-id="35dc1-117">Description</span></span>                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="35dc1-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="35dc1-118">**EnableDevice**</span></span>                                               | <span data-ttu-id="35dc1-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35dc1-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="35dc1-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="35dc1-120">**LockMedia**</span></span>](msvm-dvddrive-lockmedia.md)                   | <span data-ttu-id="35dc1-121">Verrouille ou libère le média.</span><span class="sxs-lookup"><span data-stu-id="35dc1-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="35dc1-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="35dc1-122">**OnlineDevice**</span></span>                                               | <span data-ttu-id="35dc1-123">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35dc1-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="35dc1-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="35dc1-124">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="35dc1-125">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35dc1-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="35dc1-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="35dc1-126">**RequestStateChange**</span></span>](msvm-dvddrive-requeststatechange.md) | <span data-ttu-id="35dc1-127">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="35dc1-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="35dc1-128">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="35dc1-128">**Reset**</span></span>](msvm-dvddrive-reset.md)                           | <span data-ttu-id="35dc1-129">Réinitialise l’appareil virtuel.</span><span class="sxs-lookup"><span data-stu-id="35dc1-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="35dc1-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="35dc1-130">**RestoreProperties**</span></span>                                          | <span data-ttu-id="35dc1-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35dc1-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="35dc1-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="35dc1-132">**SaveProperties**</span></span>                                             | <span data-ttu-id="35dc1-133">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35dc1-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="35dc1-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="35dc1-134">**SetPowerState**</span></span>                                              | <span data-ttu-id="35dc1-135">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="35dc1-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="35dc1-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35dc1-136">Properties</span></span>

<span data-ttu-id="35dc1-137">La classe **MSVM \_ DVDDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="35dc1-137">The **Msvm\_DVDDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35dc1-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="35dc1-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-139">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-141">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="35dc1-142">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="35dc1-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-143">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="35dc1-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-146">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-146">The primary availability and status of the device.</span></span> <span data-ttu-id="35dc1-147">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur 6 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="35dc1-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-148">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="35dc1-148">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-149">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-149">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-151">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="35dc1-151">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="35dc1-152">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="35dc1-152">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="35dc1-153">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="35dc1-153">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="35dc1-154">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="35dc1-154">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="35dc1-155">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35dc1-155">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-156">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="35dc1-156">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-157">Type de données : tableau **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35dc1-157">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-159">Fonctionnalités de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="35dc1-159">The capabilities of the media access device.</span></span> <span data-ttu-id="35dc1-160">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)et est définie avec les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="35dc1-160">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="35dc1-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="35dc1-161">Value</span></span>                                                                             | <span data-ttu-id="35dc1-162">Signification</span><span class="sxs-lookup"><span data-stu-id="35dc1-162">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35dc1-163"><dt>{3, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="35dc1-163"><dt>{3, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="35dc1-164"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="35dc1-164"><dt>3</dt></span></span> </dl>      | <span data-ttu-id="35dc1-165">L’entrée correspondante dans **CapabilityDescriptions** est « accès aléatoire ».</span><span class="sxs-lookup"><span data-stu-id="35dc1-165">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="35dc1-166"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="35dc1-166"><dt>7</dt></span></span> </dl>      | <span data-ttu-id="35dc1-167">L’entrée correspondante dans **CapabilityDescriptions** est « prend en charge les supports amovibles ».</span><span class="sxs-lookup"><span data-stu-id="35dc1-167">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="35dc1-168">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="35dc1-168">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-169">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="35dc1-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-171">Tableau de chaînes de forme libre qui fournit des explications détaillées sur l’accès aux fonctionnalités d’appareil indiquées dans le tableau de propriétés **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-171">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="35dc1-172">Chaque entrée de ce tableau est liée à l’entrée dans le tableau de propriétés des **fonctionnalités** , situé dans le même index.</span><span class="sxs-lookup"><span data-stu-id="35dc1-172">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="35dc1-173">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-173">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="35dc1-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-176">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-177">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35dc1-177">A short description of the object.</span></span> <span data-ttu-id="35dc1-178">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-179">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="35dc1-179">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-180">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-182">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="35dc1-182">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="35dc1-183">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-183">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35dc1-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-184">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-185">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="35dc1-185">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-188">Chaîne qui indique l’algorithme ou l’outil utilisé pour compresser le fichier logique.</span><span class="sxs-lookup"><span data-stu-id="35dc1-188">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="35dc1-189">Si le schéma de compression est inconnu ou n’est pas décrit, utilisez « inconnu ».</span><span class="sxs-lookup"><span data-stu-id="35dc1-189">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="35dc1-190">Si le fichier logique est compressé, mais que le schéma de compression est inconnu ou non décrit, utilisez « compressé ».</span><span class="sxs-lookup"><span data-stu-id="35dc1-190">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="35dc1-191">Si le fichier logique n’est pas compressé, utilisez « non compressé ».</span><span class="sxs-lookup"><span data-stu-id="35dc1-191">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="35dc1-192">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-192">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="35dc1-193">« Non compressé »</span><span class="sxs-lookup"><span data-stu-id="35dc1-193">"Not Compressed"</span></span>

<span data-ttu-id="35dc1-194">Connue</span><span class="sxs-lookup"><span data-stu-id="35dc1-194">"Unknown"</span></span>

<span data-ttu-id="35dc1-195">Compact</span><span class="sxs-lookup"><span data-stu-id="35dc1-195">"Compressed"</span></span>

<span data-ttu-id="35dc1-196">« Non compressé »</span><span class="sxs-lookup"><span data-stu-id="35dc1-196">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35dc1-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-198">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-199">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-200">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="35dc1-200">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="35dc1-201">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-202">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="35dc1-202">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-203">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-205">Taille de bloc par défaut, en octets, pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-205">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="35dc1-206">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-206">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-207">**Description**</span><span class="sxs-lookup"><span data-stu-id="35dc1-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-210">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="35dc1-210">A description of the object.</span></span> <span data-ttu-id="35dc1-211">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-212">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="35dc1-212">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-213">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-215">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="35dc1-215">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="35dc1-216">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35dc1-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-218">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="35dc1-218">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-221">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*».</span><span class="sxs-lookup"><span data-stu-id="35dc1-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="35dc1-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-223">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-225">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35dc1-225">A display name for the object.</span></span> <span data-ttu-id="35dc1-226">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-227">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="35dc1-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-228">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-230">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="35dc1-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="35dc1-231">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35dc1-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-232">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="35dc1-232">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-233">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-235">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="35dc1-235">The enabled and disabled states of an element.</span></span> <span data-ttu-id="35dc1-236">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="35dc1-236">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="35dc1-237">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35dc1-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="35dc1-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-239">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="35dc1-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-241">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="35dc1-242">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="35dc1-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-246">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="35dc1-246">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="35dc1-247">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-248">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="35dc1-248">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-251">Chaîne qui décrit les types de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-251">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="35dc1-252">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-252">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-253">**FormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="35dc1-253">**FormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-254">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-254">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-256">Formats CD et DVD pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-256">The CD and DVD formats that are supported by this device.</span></span> <span data-ttu-id="35dc1-257">Cette propriété est héritée de la [**\_ DVDDrive CIM**](/previous-versions//cc136812(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35dc1-257">This property is inherited from [**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85)).</span></span>

<span data-ttu-id="35dc1-258">Ce tableau contient les valeurs suivantes pour ISO.</span><span class="sxs-lookup"><span data-stu-id="35dc1-258">This array contains the following values for ISO.</span></span>

<dl> <dt>

<span data-ttu-id="35dc1-259">{16, 22}</span><span class="sxs-lookup"><span data-stu-id="35dc1-259">{16, 22}</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="35dc1-260"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="35dc1-261"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-262">Ce tableau contient les valeurs suivantes pour le transfert physique.</span><span class="sxs-lookup"><span data-stu-id="35dc1-262">This array contains the following values for physical pass-through.</span></span>

<dl> <dt>

<span data-ttu-id="35dc1-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="35dc1-263"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="35dc1-264"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span><span class="sxs-lookup"><span data-stu-id="35dc1-265"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span><span class="sxs-lookup"><span data-stu-id="35dc1-266"><span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span><span class="sxs-lookup"><span data-stu-id="35dc1-267"><span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD inscriptible** (19)</span><span class="sxs-lookup"><span data-stu-id="35dc1-268"><span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD Recordable** (19)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span><span class="sxs-lookup"><span data-stu-id="35dc1-269"><span id="DVD"></span><span id="dvd"></span>**DVD** (22)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)</span><span class="sxs-lookup"><span data-stu-id="35dc1-270"><span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW+** (23)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span><span class="sxs-lookup"><span data-stu-id="35dc1-271"><span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span><span class="sxs-lookup"><span data-stu-id="35dc1-272"><span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-vidéo** (26)</span><span class="sxs-lookup"><span data-stu-id="35dc1-273"><span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-Video** (26)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)</span><span class="sxs-lookup"><span data-stu-id="35dc1-274"><span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**Divx** (27)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span><span class="sxs-lookup"><span data-stu-id="35dc1-275"><span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span><span class="sxs-lookup"><span data-stu-id="35dc1-276"><span id="CD-DA"></span><span id="cd-da"></span>**CD-DA** (34)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-277"><span id="CD_"></span><span id="cd_"></span>**CD +** (35)</span><span class="sxs-lookup"><span data-stu-id="35dc1-277"><span id="CD_"></span><span id="cd_"></span>**CD+** (35)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD enregistrable** (36)</span><span class="sxs-lookup"><span data-stu-id="35dc1-278"><span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD Recordable** (36)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span><span class="sxs-lookup"><span data-stu-id="35dc1-279"><span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)</span><span class="sxs-lookup"><span data-stu-id="35dc1-280"><span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-Audio** (38)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span><span class="sxs-lookup"><span data-stu-id="35dc1-281"><span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span><span class="sxs-lookup"><span data-stu-id="35dc1-282"><span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span><span class="sxs-lookup"><span data-stu-id="35dc1-283"><span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span><span class="sxs-lookup"><span data-stu-id="35dc1-284"><span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35dc1-285">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="35dc1-285">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-286">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-288">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="35dc1-288">The current health of the element.</span></span> <span data-ttu-id="35dc1-289">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="35dc1-289">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="35dc1-290">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="35dc1-290">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="35dc1-291">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-292">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="35dc1-292">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-293">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="35dc1-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-295">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-295">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="35dc1-296">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35dc1-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-298">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-300">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="35dc1-300">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="35dc1-301">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-302">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35dc1-302">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-303">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-304">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-305">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="35dc1-305">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-306">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="35dc1-306">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="35dc1-307">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-307">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-308">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="35dc1-308">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-309">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-311">Date et heure du dernier nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-311">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="35dc1-312">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-312">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-313">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="35dc1-313">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-314">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35dc1-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-315">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-316">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="35dc1-316">The last error code reported by the logical device.</span></span> <span data-ttu-id="35dc1-317">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-317">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-318">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-318">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-319">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-321">Durée, en millisecondes, à partir de « Load » pour pouvoir lire ou écrire un média.</span><span class="sxs-lookup"><span data-stu-id="35dc1-321">The time, in milliseconds, from 'load' to being able to read or write a media.</span></span> <span data-ttu-id="35dc1-322">Par exemple, pour les lecteurs de disque, il s’agit de l’intervalle entre un disque qui ne tourne pas vers le disque signalant qu’il est prêt pour la lecture/écriture (c’est-à-dire le disque tournant à des vitesses nominales).</span><span class="sxs-lookup"><span data-stu-id="35dc1-322">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="35dc1-323">Pour les lecteurs de bande, il s’agit de l’heure à partir d’un support injecté pour signaler qu’il est prêt pour une application.</span><span class="sxs-lookup"><span data-stu-id="35dc1-323">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="35dc1-324">Il s’agit généralement de la zone de robot de la bande.</span><span class="sxs-lookup"><span data-stu-id="35dc1-324">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="35dc1-325">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-325">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-326">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-326">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-327">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-329">Durée, en millisecondes, à passer du premier emplacement sur le média à l’emplacement le plus éloigné par rapport au temps.</span><span class="sxs-lookup"><span data-stu-id="35dc1-329">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="35dc1-330">Pour un lecteur de disque, il s’agit de la recherche complète et du délai de rotation complète.</span><span class="sxs-lookup"><span data-stu-id="35dc1-330">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="35dc1-331">Pour les lecteurs de bande, il s’agit d’une recherche à partir du début de la bande jusqu’au point le plus éloigné physiquement.</span><span class="sxs-lookup"><span data-stu-id="35dc1-331">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="35dc1-332">(La fin d’une bande peut être à son point le plus éloigné physiquement, mais cela n’est pas nécessairement vrai.) Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-332">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-333">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="35dc1-333">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-334">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-336">Taille maximale de bloc, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-336">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="35dc1-337">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-337">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-338">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="35dc1-338">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-339">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-341">Taille maximale, en kilo-octets, des médias pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-341">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="35dc1-342">Les kilo-octets sont interprétés comme le nombre d’octets multiplié par 1000 (pas le nombre d’octets multiplié par 1024).</span><span class="sxs-lookup"><span data-stu-id="35dc1-342">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="35dc1-343">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-343">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-344">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-344">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-345">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-347">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-347">This property has been deprecated.</span></span> <span data-ttu-id="35dc1-348">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-348">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-349">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="35dc1-349">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-350">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-352">Unités maximales qui peuvent être utilisées avant le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-352">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="35dc1-353">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-353">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-354">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="35dc1-354">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-355">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="35dc1-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-357">**True** si le média est verrouillé dans l’appareil et ne peut pas être éjecté ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-357">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="35dc1-358">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-358">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-359">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="35dc1-359">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-360">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-362">Taille de bloc minimale, en octets, pour les médias accessibles par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-362">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="35dc1-363">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-363">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-364">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="35dc1-364">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-365">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-367">Pour un appareil qui prend en charge les supports amovibles, le nombre de fois que ces médias ont été montés pour le transfert de données ou pour nettoyer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-367">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="35dc1-368">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="35dc1-368">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="35dc1-369">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-369">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-370">**Nom**</span><span class="sxs-lookup"><span data-stu-id="35dc1-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-371">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-373">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="35dc1-373">The label by which the object is known.</span></span> <span data-ttu-id="35dc1-374">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-375">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="35dc1-375">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-376">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="35dc1-376">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-377">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-378">**True** si l’appareil d’accès aux médias doit être nettoyé ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-378">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="35dc1-379">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-379">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-380">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="35dc1-380">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-381">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35dc1-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-382">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-383">Nombre maximal de plusieurs médias individuels qui peuvent être pris en charge ou insérés.</span><span class="sxs-lookup"><span data-stu-id="35dc1-383">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="35dc1-384">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-384">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-385">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="35dc1-385">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-386">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-387">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-388">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-388">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="35dc1-389">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-389">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35dc1-390">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-391">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="35dc1-391">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-392">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-393">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-394">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35dc1-394">The current statuses of the object.</span></span> <span data-ttu-id="35dc1-395">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-395">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-396">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="35dc1-396">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-398">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-399">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="35dc1-399">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="35dc1-400">Cette propriété doit être définie sur **null** lorsque la propriété **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="35dc1-400">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="35dc1-401">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35dc1-401">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="35dc1-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-403">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="35dc1-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-404">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-405">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="35dc1-405">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="35dc1-406">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="35dc1-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-408">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-409">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-410">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-410">The power management capabilities of the device.</span></span> <span data-ttu-id="35dc1-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-412">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="35dc1-412">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-413">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="35dc1-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-415">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="35dc1-415">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="35dc1-416">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-416">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-417">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="35dc1-417">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-418">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-419">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-420">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="35dc1-420">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="35dc1-421">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-422">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="35dc1-422">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-423">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-425">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="35dc1-425">Provides high level status information.</span></span> <span data-ttu-id="35dc1-426">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="35dc1-426">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="35dc1-427">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-427">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35dc1-428">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-428">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-429">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="35dc1-429">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-430">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-430">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-432">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="35dc1-432">The last requested or desired state for the element.</span></span> <span data-ttu-id="35dc1-433">L’état réel de l’élément est représenté par la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-433">The actual state of the element is represented by the **EnabledState** property.</span></span> <span data-ttu-id="35dc1-434">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="35dc1-434">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="35dc1-435">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-435">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="35dc1-436">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-436">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="35dc1-437">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-437">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-438">**Sécurité**</span><span class="sxs-lookup"><span data-stu-id="35dc1-438">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-439">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-441">La sécurité opérationnelle définie pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-441">The operational security defined for the device.</span></span> <span data-ttu-id="35dc1-442">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-442">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-443">**État**</span><span class="sxs-lookup"><span data-stu-id="35dc1-443">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-444">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-445">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-446">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35dc1-446">The current status of the object.</span></span> <span data-ttu-id="35dc1-447">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-448">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="35dc1-448">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-449">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="35dc1-449">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-451">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="35dc1-451">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="35dc1-452">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35dc1-452">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="35dc1-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-454">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-456">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="35dc1-456">The current state of the logical device.</span></span> <span data-ttu-id="35dc1-457">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35dc1-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-459">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-461">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="35dc1-461">The scoping system's creation class name.</span></span> <span data-ttu-id="35dc1-462">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-463">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="35dc1-463">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-464">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-465">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-466">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="35dc1-466">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="35dc1-467">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-468">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="35dc1-468">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-469">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-469">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-471">Pour un appareil qui prend en charge les supports amovibles, la date et l’heure les plus récentes de montage du média sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-471">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="35dc1-472">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’a aucune signification et n’est pas applicable.</span><span class="sxs-lookup"><span data-stu-id="35dc1-472">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="35dc1-473">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-473">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-474">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="35dc1-474">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-475">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-476">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-477">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="35dc1-477">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="35dc1-478">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-479">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-479">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-480">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-482">Pour un appareil qui prend en charge les supports amovibles, durée totale (en secondes) de montage des médias pour le transfert de données ou le nettoyage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-482">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="35dc1-483">Pour les appareils qui accèdent à des médias non amovibles, tels que des disques durs, cette propriété n’est pas applicable et doit être définie sur 0.</span><span class="sxs-lookup"><span data-stu-id="35dc1-483">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="35dc1-484">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-484">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="35dc1-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-486">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-487">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-488">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="35dc1-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="35dc1-489">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="35dc1-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-491">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35dc1-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-493">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="35dc1-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="35dc1-494">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="35dc1-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-495">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="35dc1-495">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-496">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35dc1-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-497">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-498">Taux de transfert de données soutenu, en Ko/s, que l’appareil peut lire et écrire sur un média.</span><span class="sxs-lookup"><span data-stu-id="35dc1-498">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="35dc1-499">Il s’agit d’un débit de données brutes soutenu.</span><span class="sxs-lookup"><span data-stu-id="35dc1-499">This is a sustained, raw data rate.</span></span> <span data-ttu-id="35dc1-500">Les taux ou taux maximaux en supposant que la compression ne doit pas être signalée dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="35dc1-500">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="35dc1-501">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-501">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-502">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="35dc1-502">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-503">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35dc1-503">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-504">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-505">Unités relatives à son utilisation dans **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="35dc1-505">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="35dc1-506">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-506">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-507">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="35dc1-507">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-508">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-509">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-510">Nombre actuel d’unités utilisées.</span><span class="sxs-lookup"><span data-stu-id="35dc1-510">The current number of units used.</span></span> <span data-ttu-id="35dc1-511">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-511">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="35dc1-512">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="35dc1-512">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35dc1-513">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35dc1-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35dc1-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35dc1-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35dc1-515">Durée, en millisecondes, de la possibilité de lire ou d’écrire un média dans son « déchargement ».</span><span class="sxs-lookup"><span data-stu-id="35dc1-515">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="35dc1-516">Cette propriété est héritée de la [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="35dc1-516">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35dc1-517">Notes</span><span class="sxs-lookup"><span data-stu-id="35dc1-517">Remarks</span></span>

<span data-ttu-id="35dc1-518">L’accès à la classe **MSVM \_ DVDDrive** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="35dc1-518">Access to the **Msvm\_DVDDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="35dc1-519">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="35dc1-519">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="35dc1-520">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35dc1-520">Requirements</span></span>



| <span data-ttu-id="35dc1-521">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35dc1-521">Requirement</span></span> | <span data-ttu-id="35dc1-522">Valeur</span><span class="sxs-lookup"><span data-stu-id="35dc1-522">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dc1-523">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35dc1-523">Minimum supported client</span></span><br/> | <span data-ttu-id="35dc1-524">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35dc1-524">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35dc1-525">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35dc1-525">Minimum supported server</span></span><br/> | <span data-ttu-id="35dc1-526">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35dc1-526">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35dc1-527">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35dc1-527">Namespace</span></span><br/>                | <span data-ttu-id="35dc1-528">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="35dc1-528">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35dc1-529">MOF</span><span class="sxs-lookup"><span data-stu-id="35dc1-529">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35dc1-530"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35dc1-530"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35dc1-531">DLL</span><span class="sxs-lookup"><span data-stu-id="35dc1-531">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35dc1-532"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35dc1-532"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35dc1-533">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35dc1-533">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dc1-534">**\_DVDDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="35dc1-534">**CIM\_DVDDrive**</span></span>](cim-dvddrive.md)
</dt> <dt>

<span data-ttu-id="35dc1-535">[**\_DVDDRIVE CIM**](/previous-versions//cc136812(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35dc1-535">[**CIM\_DVDDrive**](/previous-versions//cc136812(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="35dc1-536">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="35dc1-536">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

