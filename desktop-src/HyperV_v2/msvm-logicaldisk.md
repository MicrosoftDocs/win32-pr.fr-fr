---
description: Représente un support de lecteur de stockage et est utilisé pour alimenter les lecteurs de stockage.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Msvm_LogicalDisk, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534539"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="70451-103">\_Classe LogicalDisk MSVM</span><span class="sxs-lookup"><span data-stu-id="70451-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="70451-104">Représente un support de lecteur de stockage et est utilisé pour alimenter les lecteurs de stockage.</span><span class="sxs-lookup"><span data-stu-id="70451-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="70451-105">Les types de médias pris en charge incluent les fichiers de disque dur virtuel, les fichiers de disquette virtuelle, les fichiers ISO et les supports de l’appareil physique.</span><span class="sxs-lookup"><span data-stu-id="70451-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="70451-106">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="70451-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70451-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70451-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  uint16   CreationClassName = "Msvm_LogicalDisk";
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
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="70451-108">Membres</span><span class="sxs-lookup"><span data-stu-id="70451-108">Members</span></span>

<span data-ttu-id="70451-109">La classe **MSVM \_ LogicalDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70451-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="70451-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70451-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="70451-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70451-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="70451-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="70451-112">Methods</span></span>

<span data-ttu-id="70451-113">La **classe \_ LogicalDisk MSVM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="70451-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="70451-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="70451-114">Method</span></span>                                                            | <span data-ttu-id="70451-115">Description</span><span class="sxs-lookup"><span data-stu-id="70451-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="70451-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="70451-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="70451-117">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70451-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="70451-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="70451-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="70451-119">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70451-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="70451-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="70451-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="70451-121">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70451-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="70451-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="70451-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="70451-123">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="70451-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="70451-124">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="70451-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="70451-125">Réinitialise le service.</span><span class="sxs-lookup"><span data-stu-id="70451-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="70451-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="70451-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="70451-127">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70451-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="70451-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="70451-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="70451-129">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70451-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="70451-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="70451-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="70451-131">Cette méthode n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70451-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="70451-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70451-132">Properties</span></span>

<span data-ttu-id="70451-133">La **classe \_ LogicalDisk MSVM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="70451-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70451-134">**y accéder**</span><span class="sxs-lookup"><span data-stu-id="70451-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-135">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-137">Indique si le média est lisible, accessible en écriture ou les deux.</span><span class="sxs-lookup"><span data-stu-id="70451-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="70451-138">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="70451-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-139">Value</span></span>                                                                        | <span data-ttu-id="70451-140">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="70451-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70451-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="70451-142">Unknown</span><span class="sxs-lookup"><span data-stu-id="70451-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="70451-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70451-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="70451-144">R.a..</span><span class="sxs-lookup"><span data-stu-id="70451-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="70451-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="70451-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="70451-146">Accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="70451-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="70451-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="70451-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="70451-148">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="70451-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="70451-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="70451-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="70451-150">Écriture unique.</span><span class="sxs-lookup"><span data-stu-id="70451-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="70451-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-152">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-154">Disponibilité et état supplémentaires de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70451-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="70451-155">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="70451-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="70451-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-156">Value</span></span>                                                                            | <span data-ttu-id="70451-157">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="70451-158"><dt>6,3</dt></span><span class="sxs-lookup"><span data-stu-id="70451-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="70451-159">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="70451-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-160">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="70451-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-161">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-163">Disponibilité et état principaux de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70451-163">The primary availability and status of the device.</span></span> <span data-ttu-id="70451-164">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="70451-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="70451-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-165">Value</span></span>                                                                        | <span data-ttu-id="70451-166">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="70451-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="70451-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="70451-168">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="70451-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-169">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="70451-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-170">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-172">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) utilisée pour initier un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="70451-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="70451-173">Les valeurs répertoriées sont un sous-ensemble des valeurs contenues dans la propriété **RequestedStatesSupported** de l’instance associée de la **\_ EnabledLogicalElementCapabilities CIM**, où les valeurs sélectionnées sont une fonction de l’état actuel de l’objet [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="70451-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="70451-174">Cette propriété peut être non **null** si une implémentation est en mesure de publier l’ensemble de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="70451-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="70451-175">Cette propriété a la **valeur null** si une implémentation ne peut pas déterminer le jeu de valeurs possibles en tant que fonction de l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="70451-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="70451-176">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70451-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="70451-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="70451-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-178">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-180">Taille, en octets, des blocs qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="70451-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="70451-181">Si la taille de bloc est variable, la taille de bloc maximale, en octets, doit être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="70451-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="70451-182">Si la taille de bloc est inconnue ou si un concept de bloc n’est pas valide (par exemple, pour les extensions d’agrégat, la mémoire ou les disques logiques), cela contient 1.</span><span class="sxs-lookup"><span data-stu-id="70451-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="70451-183">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="70451-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-187">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70451-187">A short description of the object.</span></span> <span data-ttu-id="70451-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="70451-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="70451-189">« Image de disque ISO »</span><span class="sxs-lookup"><span data-stu-id="70451-189">"ISO Disk Image"</span></span>

<span data-ttu-id="70451-190">« Image de disque dur »</span><span class="sxs-lookup"><span data-stu-id="70451-190">"Hard Disk Image"</span></span>

<span data-ttu-id="70451-191">« Image disquette »</span><span class="sxs-lookup"><span data-stu-id="70451-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="70451-192">« CD/DVD »</span><span class="sxs-lookup"><span data-stu-id="70451-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="70451-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="70451-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-194">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-196">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="70451-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="70451-197">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="70451-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="70451-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-199">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="70451-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-200">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-202">Nombre maximal de blocs, de tailles de **bloc**, qui sont disponibles pour la consommation lors de la superposition des extensions de stockage à l’aide de l’Association [**MSVM \_ BasedOn**](msvm-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="70451-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="70451-203">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-204">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70451-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-205">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-207">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="70451-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="70451-208">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="70451-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="70451-209">**DataOrganization**</span><span class="sxs-lookup"><span data-stu-id="70451-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-210">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-212">Type d’organisation de données utilisé.</span><span class="sxs-lookup"><span data-stu-id="70451-212">The type of data organization used.</span></span> <span data-ttu-id="70451-213">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="70451-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-214">Value</span></span>                                                                        | <span data-ttu-id="70451-215">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="70451-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="70451-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="70451-217">Bloc fixe.</span><span class="sxs-lookup"><span data-stu-id="70451-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-218">**DataRedundancy**</span><span class="sxs-lookup"><span data-stu-id="70451-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-219">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-221">Nombre total de copies de données actuellement gérées.</span><span class="sxs-lookup"><span data-stu-id="70451-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="70451-222">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-223">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="70451-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-224">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="70451-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="70451-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-226">Pourcentage qui spécifie la quantité d’espace qui doit être réservée dans un réplica pour la mise en cache des modifications.</span><span class="sxs-lookup"><span data-stu-id="70451-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="70451-227">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-228">**Description**</span><span class="sxs-lookup"><span data-stu-id="70451-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-229">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-231">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="70451-231">A description of the object.</span></span> <span data-ttu-id="70451-232">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="70451-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="70451-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-234">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-236">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="70451-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="70451-237">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="70451-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="70451-238">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-239">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="70451-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-242">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur « Microsoft :*GUID* \\ *Device-Specific-Data*».</span><span class="sxs-lookup"><span data-stu-id="70451-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="70451-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="70451-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-246">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70451-246">A display name for the object.</span></span> <span data-ttu-id="70451-247">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="70451-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="70451-248">« Image de disque ISO »</span><span class="sxs-lookup"><span data-stu-id="70451-248">"ISO Disk Image"</span></span>

<span data-ttu-id="70451-249">« Image de disque dur »</span><span class="sxs-lookup"><span data-stu-id="70451-249">"Hard Disk Image"</span></span>

<span data-ttu-id="70451-250">« Image disquette »</span><span class="sxs-lookup"><span data-stu-id="70451-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="70451-251">« CD/DVD »</span><span class="sxs-lookup"><span data-stu-id="70451-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="70451-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="70451-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-253">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-255">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="70451-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="70451-256">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70451-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="70451-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="70451-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-260">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="70451-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="70451-261">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="70451-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="70451-262">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70451-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="70451-263">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="70451-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-264">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70451-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70451-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-266">Indique si l’erreur signalée dans **LastErrorCode** est maintenant désactivée.</span><span class="sxs-lookup"><span data-stu-id="70451-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="70451-267">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="70451-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-269">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-270">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-271">Chaîne qui fournit des informations supplémentaires sur l’erreur enregistrée dans **LastErrorCode** et des informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="70451-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="70451-272">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-273">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="70451-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-276">Chaîne qui décrit les types de détection d’erreurs et de correction pris en charge par cet appareil.</span><span class="sxs-lookup"><span data-stu-id="70451-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="70451-277">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-278">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="70451-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-279">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-281">Toutes les informations d’État supplémentaires au-delà de celles capturées dans le **OperationalStatus** et d’autres propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="70451-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="70451-282">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-282">Value</span></span>                                                                            | <span data-ttu-id="70451-283">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="70451-284"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="70451-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="70451-285">Aucun/non applicable.</span><span class="sxs-lookup"><span data-stu-id="70451-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="70451-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-287">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-289">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="70451-289">The current health of the element.</span></span> <span data-ttu-id="70451-290">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="70451-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="70451-291">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="70451-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="70451-292">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="70451-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-294">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="70451-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-296">Tableau de chaînes de forme libre qui fournissent des explications et des détails sur les entrées du tableau de propriétés **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="70451-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="70451-297">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="70451-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="70451-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="70451-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-299">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70451-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70451-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-301">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="70451-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="70451-302">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="70451-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70451-306">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="70451-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="70451-307">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="70451-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="70451-308">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="70451-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-309">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="70451-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-310">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70451-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70451-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-312">Indique si les extensions de stockage sous-jacentes participent à un groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="70451-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="70451-313">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="70451-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-315">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70451-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70451-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-317">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="70451-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="70451-318">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-319">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="70451-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-320">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-322">Cette propriété est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="70451-322">This property has been deprecated.</span></span> <span data-ttu-id="70451-323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-324">**Nom**</span><span class="sxs-lookup"><span data-stu-id="70451-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-327">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="70451-327">The label by which the object is known.</span></span> <span data-ttu-id="70451-328">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est identique à la propriété **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="70451-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="70451-329">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="70451-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-330">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-331">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-332">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="70451-333">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-333">Value</span></span>                                                                         | <span data-ttu-id="70451-334">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="70451-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70451-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="70451-336">Autres</span><span class="sxs-lookup"><span data-stu-id="70451-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="70451-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="70451-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="70451-338">Nom du périphérique du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="70451-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-339">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="70451-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-340">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-341">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-342">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="70451-343">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-343">Value</span></span>                                                                        | <span data-ttu-id="70451-344">Signification</span><span class="sxs-lookup"><span data-stu-id="70451-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="70451-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="70451-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="70451-346">Autres</span><span class="sxs-lookup"><span data-stu-id="70451-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="70451-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="70451-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="70451-348">Espace de noms du périphérique du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="70451-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="70451-349">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="70451-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-350">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70451-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70451-351">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-352">Indique s’il n’existe aucun point de défaillance unique.</span><span class="sxs-lookup"><span data-stu-id="70451-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="70451-353">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="70451-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-355">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-357">Nombre de blocs consécutifs, chacun bloquant la taille de la valeur contenue dans la propriété **BlockSize** , qui forment l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="70451-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="70451-358">La taille totale de l’extension de stockage peut être calculée en multipliant la valeur de la propriété **BlockSize** par la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="70451-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="70451-359">Si la valeur de **BlockSize** est 1, cette propriété correspond à la taille totale de l’extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="70451-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="70451-360">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-361">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="70451-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-362">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-364">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="70451-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="70451-365">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="70451-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="70451-366">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="70451-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-368">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-369">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70451-370">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span><span class="sxs-lookup"><span data-stu-id="70451-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="70451-371">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70451-371">The current statuses of the object.</span></span> <span data-ttu-id="70451-372">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="70451-373">Lorsque le niveau de QoS requis pour le disque virtuel ne peut pas être respecté, l’état principal (OperationalStatus \[ 0 \] ) est défini sur détérioré (3) et le tableau OperationalStatus contient une valeur d’état secondaire qui indique la raison spécifique de la condition de QoS, en fonction de cette table.</span><span class="sxs-lookup"><span data-stu-id="70451-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="70451-374">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="70451-375">Description</span><span class="sxs-lookup"><span data-stu-id="70451-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70451-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Débit insuffisant (32788)</span><span class="sxs-lookup"><span data-stu-id="70451-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="70451-377">Le taux d’e/s par seconde minimal demandé n’est actuellement pas disponible pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70451-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="70451-378">OperationalStatus est également utilisé pour signaler d’autres conditions d’erreur ou d’avertissement (par exemple, une incompatibilité de protocole entre VSP et VSC).</span><span class="sxs-lookup"><span data-stu-id="70451-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="70451-379">Si plusieurs conditions existent, l’état principal est défini sur détérioré et une ou plusieurs valeurs d’État secondaires, dans n’importe quel ordre commençant à l’index 1, sont remplies dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="70451-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="70451-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="70451-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="70451-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (3)</span><span class="sxs-lookup"><span data-stu-id="70451-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="70451-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (7)</span><span class="sxs-lookup"><span data-stu-id="70451-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="70451-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (11)</span><span class="sxs-lookup"><span data-stu-id="70451-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="70451-384">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70451-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="70451-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (12)</span><span class="sxs-lookup"><span data-stu-id="70451-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="70451-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Perte de communication** (13)</span><span class="sxs-lookup"><span data-stu-id="70451-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="70451-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (16)</span><span class="sxs-lookup"><span data-stu-id="70451-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="70451-388">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70451-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="70451-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Incompatibilité de protocole** (32775)</span><span class="sxs-lookup"><span data-stu-id="70451-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="70451-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>Expiration du **délai de communication** (32783)</span><span class="sxs-lookup"><span data-stu-id="70451-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="70451-391">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70451-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="70451-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Débit insuffisant** (32788)</span><span class="sxs-lookup"><span data-stu-id="70451-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="70451-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**ID de stratégie QoS inconnu** (32791)</span><span class="sxs-lookup"><span data-stu-id="70451-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="70451-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS non prise en charge** (32792)</span><span class="sxs-lookup"><span data-stu-id="70451-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="70451-395">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70451-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="70451-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**Incompatibilité de configuration QoS** (32793)</span><span class="sxs-lookup"><span data-stu-id="70451-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="70451-397">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70451-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="70451-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disque plein** (32794)</span><span class="sxs-lookup"><span data-stu-id="70451-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="70451-399">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="70451-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="70451-400">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="70451-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-402">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-403">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="70451-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="70451-404">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="70451-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="70451-405">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70451-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="70451-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="70451-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-407">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="70451-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-408">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-409">Toutes les données supplémentaires, au-delà des informations d’ID d’appareil, qui peuvent être utilisées pour identifier un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="70451-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="70451-410">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)et est définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="70451-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="70451-411">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="70451-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-413">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-414">Chaîne qui décrit le format de la propriété **Name** lorsque **NameFormat** contient la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="70451-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="70451-415">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-416">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="70451-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-417">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-418">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-419">Chaîne qui décrit l’espace de noms de la propriété **Name** lorsque **NameNamespace** contient la valeur 1 (other).</span><span class="sxs-lookup"><span data-stu-id="70451-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="70451-420">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-421">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="70451-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-422">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-423">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-424">Nombre de packages physiques qui peuvent échouer actuellement sans perte de données.</span><span class="sxs-lookup"><span data-stu-id="70451-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="70451-425">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-426">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="70451-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-427">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-428">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-429">Les fonctionnalités de gestion de l’alimentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="70451-429">The power management capabilities of the device.</span></span> <span data-ttu-id="70451-430">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="70451-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-432">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70451-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70451-433">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-434">Indique si l’appareil peut être géré par l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="70451-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="70451-435">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="70451-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-437">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-438">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-439">Nombre d’heures consécutives de mise sous tension de cet appareil depuis son dernier cycle d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="70451-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="70451-440">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-441">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="70451-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-442">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-443">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-444">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="70451-444">Provides high level status information.</span></span> <span data-ttu-id="70451-445">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir des informations d’état d’intégrité de haut niveau et détaillées pour l’élément et ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="70451-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="70451-446">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="70451-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="70451-447">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-448">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="70451-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-449">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70451-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70451-450">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-451">Indique si le système conteneur a la capacité de créer ou de supprimer cet élément opérationnel.</span><span class="sxs-lookup"><span data-stu-id="70451-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="70451-452">Cette propriété est héritée de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)et est définie sur **false** pour les médias basés sur des fichiers et **true** pour les médias directs.</span><span class="sxs-lookup"><span data-stu-id="70451-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="70451-453">**Objectif**</span><span class="sxs-lookup"><span data-stu-id="70451-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-454">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-455">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-456">Chaîne qui décrit le média et/ou son utilisation.</span><span class="sxs-lookup"><span data-stu-id="70451-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="70451-457">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="70451-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-459">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-460">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-461">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="70451-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="70451-462">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="70451-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="70451-463">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="70451-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="70451-464">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="70451-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="70451-465">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="70451-466">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="70451-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="70451-467">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="70451-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-468">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="70451-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="70451-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-470">Indique si le stockage est accessible de manière séquentielle par un appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="70451-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="70451-471">Un support de bande direct est un exemple d’extension de stockage à accès séquentiel.</span><span class="sxs-lookup"><span data-stu-id="70451-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="70451-472">Cette propriété est héritée de la [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="70451-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="70451-473">**État**</span><span class="sxs-lookup"><span data-stu-id="70451-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-474">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-475">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-476">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70451-476">The current status of the object.</span></span> <span data-ttu-id="70451-477">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-478">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="70451-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-479">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="70451-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="70451-480">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-481">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="70451-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="70451-482">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="70451-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="70451-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="70451-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-484">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-485">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-486">État actuel de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="70451-486">The current state of the logical device.</span></span> <span data-ttu-id="70451-487">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-488">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="70451-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-489">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-490">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-491">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="70451-491">The scoping system's creation class name.</span></span> <span data-ttu-id="70451-492">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="70451-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="70451-493">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="70451-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-494">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="70451-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70451-495">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-496">Identificateur unique de la machine virtuelle d’étendue.</span><span class="sxs-lookup"><span data-stu-id="70451-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="70451-497">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="70451-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="70451-498">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="70451-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-499">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70451-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="70451-500">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-501">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="70451-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="70451-502">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="70451-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="70451-503">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="70451-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-504">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="70451-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="70451-505">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-506">Nombre total d’heures d’alimentation de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="70451-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="70451-507">Cette propriété est héritée de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="70451-508">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="70451-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70451-509">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="70451-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="70451-510">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="70451-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70451-511">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="70451-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="70451-512">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="70451-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70451-513">Notes</span><span class="sxs-lookup"><span data-stu-id="70451-513">Remarks</span></span>

<span data-ttu-id="70451-514">L’accès à la classe **MSVM \_ LogicalDisk** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="70451-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="70451-515">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="70451-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="70451-516">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70451-516">Requirements</span></span>



| <span data-ttu-id="70451-517">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70451-517">Requirement</span></span> | <span data-ttu-id="70451-518">Valeur</span><span class="sxs-lookup"><span data-stu-id="70451-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70451-519">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70451-519">Minimum supported client</span></span><br/> | <span data-ttu-id="70451-520">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70451-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="70451-521">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70451-521">Minimum supported server</span></span><br/> | <span data-ttu-id="70451-522">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70451-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70451-523">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="70451-523">Namespace</span></span><br/>                | <span data-ttu-id="70451-524">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="70451-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="70451-525">MOF</span><span class="sxs-lookup"><span data-stu-id="70451-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70451-526"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70451-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="70451-527">DLL</span><span class="sxs-lookup"><span data-stu-id="70451-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70451-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="70451-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="70451-529">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70451-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70451-530">**\_Disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="70451-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="70451-531">**\_Disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="70451-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="70451-532">**MSVM \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="70451-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="70451-533">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="70451-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

