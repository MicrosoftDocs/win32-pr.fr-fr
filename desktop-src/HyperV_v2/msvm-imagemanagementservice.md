---
description: Gère les fichiers de média virtuel (. vhd,. vhdx,. ISO ou. VFD) pour un ordinateur virtuel.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752372"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="dce3a-103">MSVM \_ ImageManagementService, classe</span><span class="sxs-lookup"><span data-stu-id="dce3a-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="dce3a-104">Gère les fichiers de média virtuel (. vhd,. vhdx,. ISO ou. VFD) pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="dce3a-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dce3a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce3a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dce3a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="dce3a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="dce3a-107">Members</span></span>

<span data-ttu-id="dce3a-108">La classe **MSVM \_ ImageManagementService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dce3a-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="dce3a-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dce3a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="dce3a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dce3a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dce3a-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dce3a-111">Methods</span></span>

<span data-ttu-id="dce3a-112">La classe **MSVM \_ ImageManagementService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dce3a-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="dce3a-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="dce3a-113">Method</span></span>                                                                                                           | <span data-ttu-id="dce3a-114">Description</span><span class="sxs-lookup"><span data-stu-id="dce3a-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dce3a-115">**AttachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="dce3a-116">Joint un fichier image de disque virtuel en mode de bouclage.</span><span class="sxs-lookup"><span data-stu-id="dce3a-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="dce3a-117">**CompactVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="dce3a-118">Compacte un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="dce3a-119">**ConvertVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="dce3a-120">Convertit un disque dur virtuel existant dans un autre type ou format.</span><span class="sxs-lookup"><span data-stu-id="dce3a-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="dce3a-121">**ConvertVirtualHardDiskToVHDSet**</span><span class="sxs-lookup"><span data-stu-id="dce3a-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="dce3a-122">Convertit un fichier de disque dur virtuel en créant un nouveau fichier de définition de disque dur virtuel en même temps que le disque dur virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="dce3a-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="dce3a-123">**CreateVirtualFloppyDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="dce3a-124">Crée un fichier de disquette virtuelle.</span><span class="sxs-lookup"><span data-stu-id="dce3a-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="dce3a-125">**CreateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="dce3a-126">Crée un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="dce3a-127">**DeleteVHDSnapshot**</span><span class="sxs-lookup"><span data-stu-id="dce3a-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="dce3a-128">Supprime une entrée de capture instantanée de disque dur virtuel dans un fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="dce3a-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="dce3a-129">**FindMountedStorageImageInstance**</span><span class="sxs-lookup"><span data-stu-id="dce3a-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="dce3a-130">Recherche un \_ objet MSVM MountedStorageImage pour un chemin d’accès d’image de disque donné.</span><span class="sxs-lookup"><span data-stu-id="dce3a-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="dce3a-131">**GetVHDSetInformation**</span><span class="sxs-lookup"><span data-stu-id="dce3a-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="dce3a-132">Récupère des informations sur un fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="dce3a-133">**GetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="dce3a-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="dce3a-134">Récupère des informations sur une capture instantanée de disque dur virtuel dans un fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="dce3a-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="dce3a-135">**GetVirtualDiskChanges**</span><span class="sxs-lookup"><span data-stu-id="dce3a-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="dce3a-136">Récupère une liste de modifications dans la région spécifiée d’un disque virtuel depuis l’ID de Change Tracking résilient fourni ou l’ID d’instantané VHDSet.</span><span class="sxs-lookup"><span data-stu-id="dce3a-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="dce3a-137">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="dce3a-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="dce3a-138">Récupère les données de paramètre associées aux fichiers de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="dce3a-139">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="dce3a-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="dce3a-140">Récupère l’état des fichiers de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="dce3a-141">**MergeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="dce3a-142">Fusionne un disque dur virtuel enfant dans une chaîne de différenciation avec un ou plusieurs disques durs virtuels parents dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="dce3a-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="dce3a-143">**OptimizeVHDSet**</span><span class="sxs-lookup"><span data-stu-id="dce3a-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="dce3a-144">Optimise un fichier de définition de disque dur virtuel pour utiliser moins d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="dce3a-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="dce3a-145">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="dce3a-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="dce3a-146">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="dce3a-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="dce3a-147">**ResizeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="dce3a-148">Redimensionne un disque dur virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="dce3a-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="dce3a-149">**SetParentVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="dce3a-150">Met à jour le parent pour les fichiers de disque dur virtuel enfants et de feuille spécifiés.</span><span class="sxs-lookup"><span data-stu-id="dce3a-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="dce3a-151">**SetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="dce3a-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="dce3a-152">Modifie une entrée d’instantané de disque dur virtuel dans un fichier de définition de VHD.</span><span class="sxs-lookup"><span data-stu-id="dce3a-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="dce3a-153">Si l’ID d’instantané en question existe déjà, l’entrée d’instantané existante sera remplacée par la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="dce3a-154">Dans le cas contraire, la nouvelle entrée sera ajoutée au fichier de définition de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="dce3a-155">**SetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="dce3a-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="dce3a-156">Définit un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="dce3a-157">**StartService**</span><span class="sxs-lookup"><span data-stu-id="dce3a-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="dce3a-158">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="dce3a-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="dce3a-159">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dce3a-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="dce3a-160">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="dce3a-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="dce3a-161">**ValidatePersistentReservationSupport**</span><span class="sxs-lookup"><span data-stu-id="dce3a-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="dce3a-162">Valide si un système de fichiers peut prendre en charge un disque dur virtuel pour lequel les réservations persistantes sont activées.</span><span class="sxs-lookup"><span data-stu-id="dce3a-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="dce3a-163">**ValidateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="dce3a-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="dce3a-164">Valide si une image de disque virtuel peut être ouverte en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="dce3a-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="dce3a-165">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dce3a-165">Properties</span></span>

<span data-ttu-id="dce3a-166">La classe **MSVM \_ ImageManagementService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="dce3a-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dce3a-167">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="dce3a-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-168">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-170">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dce3a-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="dce3a-171">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dce3a-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-175">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dce3a-175">A short description of the object.</span></span> <span data-ttu-id="dce3a-176">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur le « service de gestion d’images Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="dce3a-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="dce3a-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-178">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-180">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="dce3a-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dce3a-181">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dce3a-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dce3a-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="dce3a-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="dce3a-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span><span class="sxs-lookup"><span data-stu-id="dce3a-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Communication perdue** (3)</span><span class="sxs-lookup"><span data-stu-id="dce3a-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (4)</span><span class="sxs-lookup"><span data-stu-id="dce3a-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="dce3a-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dce3a-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dce3a-190">)</span><span class="sxs-lookup"><span data-stu-id="dce3a-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dce3a-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dce3a-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-194">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="dce3a-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dce3a-195">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ImageManagementService ».</span><span class="sxs-lookup"><span data-stu-id="dce3a-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-196">**Description**</span><span class="sxs-lookup"><span data-stu-id="dce3a-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-199">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="dce3a-199">A description of the object.</span></span> <span data-ttu-id="dce3a-200">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), et elle est toujours définie sur « assure la maintenance de la gestion d’images pour Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="dce3a-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dce3a-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-204">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="dce3a-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dce3a-205">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dce3a-206">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dce3a-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="dce3a-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Aucune information supplémentaire** (1)</span><span class="sxs-lookup"><span data-stu-id="dce3a-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Souligné** (2)</span><span class="sxs-lookup"><span data-stu-id="dce3a-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Défaillance prédictive** (3)</span><span class="sxs-lookup"><span data-stu-id="dce3a-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Erreur non récupérable** (4)</span><span class="sxs-lookup"><span data-stu-id="dce3a-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entité de prise en charge erronée** (5)</span><span class="sxs-lookup"><span data-stu-id="dce3a-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="dce3a-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dce3a-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dce3a-215">)</span><span class="sxs-lookup"><span data-stu-id="dce3a-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dce3a-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dce3a-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-219">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dce3a-219">A display name for the object.</span></span> <span data-ttu-id="dce3a-220">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur le « service de gestion d’images Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="dce3a-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="dce3a-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-222">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-224">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="dce3a-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="dce3a-225">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="dce3a-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dce3a-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-227">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-229">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="dce3a-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="dce3a-230">Il peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="dce3a-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="dce3a-231">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="dce3a-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dce3a-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-233">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-235">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="dce3a-235">The current health of the element.</span></span> <span data-ttu-id="dce3a-236">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="dce3a-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dce3a-237">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dce3a-238">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5.</span><span class="sxs-lookup"><span data-stu-id="dce3a-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dce3a-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-240">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dce3a-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-242">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dce3a-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="dce3a-243">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dce3a-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-247">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="dce3a-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-248">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="dce3a-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dce3a-249">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-250">**Nom**</span><span class="sxs-lookup"><span data-stu-id="dce3a-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-253">Qualificateurs : **clé**, **remplacement** ("nom"), **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="dce3a-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-254">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="dce3a-254">The label by which the object is known.</span></span> <span data-ttu-id="dce3a-255">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « vhdsvc ».</span><span class="sxs-lookup"><span data-stu-id="dce3a-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="dce3a-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-257">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-259">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="dce3a-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dce3a-260">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dce3a-261">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dce3a-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="dce3a-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="dce3a-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Maintenance** (2)</span><span class="sxs-lookup"><span data-stu-id="dce3a-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Démarrage** (3)</span><span class="sxs-lookup"><span data-stu-id="dce3a-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arrêt** (4)</span><span class="sxs-lookup"><span data-stu-id="dce3a-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrêté** (5)</span><span class="sxs-lookup"><span data-stu-id="dce3a-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abandonné** (6)</span><span class="sxs-lookup"><span data-stu-id="dce3a-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span><span class="sxs-lookup"><span data-stu-id="dce3a-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Terminé** (8)</span><span class="sxs-lookup"><span data-stu-id="dce3a-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migration** (9)</span><span class="sxs-lookup"><span data-stu-id="dce3a-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="dce3a-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Inmigration** (11)</span><span class="sxs-lookup"><span data-stu-id="dce3a-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Capture d’instantanés** (12)</span><span class="sxs-lookup"><span data-stu-id="dce3a-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arrêt** (13)</span><span class="sxs-lookup"><span data-stu-id="dce3a-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (14)</span><span class="sxs-lookup"><span data-stu-id="dce3a-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transition** (15)</span><span class="sxs-lookup"><span data-stu-id="dce3a-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En service** (16)</span><span class="sxs-lookup"><span data-stu-id="dce3a-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="dce3a-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dce3a-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dce3a-281">)</span><span class="sxs-lookup"><span data-stu-id="dce3a-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dce3a-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dce3a-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-283">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-285">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dce3a-285">The current status of the object.</span></span> <span data-ttu-id="dce3a-286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="dce3a-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="dce3a-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-290">État activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="dce3a-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="dce3a-291">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="dce3a-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="dce3a-292">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="dce3a-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-296">Chaîne qui fournit des informations sur la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="dce3a-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="dce3a-297">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-298">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="dce3a-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-299">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-300">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-301">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="dce3a-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="dce3a-302">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="dce3a-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="dce3a-303">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-304">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="dce3a-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-305">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-307">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="dce3a-307">Provides high level status information.</span></span> <span data-ttu-id="dce3a-308">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="dce3a-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dce3a-309">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dce3a-310">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dce3a-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="dce3a-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="dce3a-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (2)</span><span class="sxs-lookup"><span data-stu-id="dce3a-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (3)</span><span class="sxs-lookup"><span data-stu-id="dce3a-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="dce3a-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fournisseur réservé** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dce3a-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dce3a-317">)</span><span class="sxs-lookup"><span data-stu-id="dce3a-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dce3a-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="dce3a-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-319">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-321">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="dce3a-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="dce3a-322">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="dce3a-323">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="dce3a-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="dce3a-324">Une instance particulière de **EnabledLogicalElement** peut ne pas prendre en charge **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="dce3a-325">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="dce3a-326">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="dce3a-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-327">**Cours**</span><span class="sxs-lookup"><span data-stu-id="dce3a-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-328">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dce3a-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-329">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-330">Indique si le service a été démarré.</span><span class="sxs-lookup"><span data-stu-id="dce3a-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="dce3a-331">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-332">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="dce3a-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-334">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-335">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="dce3a-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="dce3a-336">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-337">**État**</span><span class="sxs-lookup"><span data-stu-id="dce3a-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-340">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dce3a-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dce3a-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-342">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="dce3a-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-344">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="dce3a-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dce3a-345">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dce3a-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dce3a-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-347">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-348">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-349">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="dce3a-349">The scoping system's creation class name.</span></span> <span data-ttu-id="dce3a-350">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="dce3a-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dce3a-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dce3a-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-354">Nom du système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="dce3a-354">The name of the hosting computer system.</span></span> <span data-ttu-id="dce3a-355">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dce3a-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="dce3a-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-357">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dce3a-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-358">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-359">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="dce3a-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="dce3a-360">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dce3a-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dce3a-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="dce3a-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce3a-362">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dce3a-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dce3a-363">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dce3a-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce3a-364">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="dce3a-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="dce3a-365">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="dce3a-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dce3a-366">Notes</span><span class="sxs-lookup"><span data-stu-id="dce3a-366">Remarks</span></span>

<span data-ttu-id="dce3a-367">L’accès à la classe **MSVM \_ ImageManagementService** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="dce3a-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dce3a-368">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dce3a-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dce3a-369">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dce3a-369">Requirements</span></span>



| <span data-ttu-id="dce3a-370">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dce3a-370">Requirement</span></span> | <span data-ttu-id="dce3a-371">Valeur</span><span class="sxs-lookup"><span data-stu-id="dce3a-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce3a-372">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dce3a-372">Minimum supported client</span></span><br/> | <span data-ttu-id="dce3a-373">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dce3a-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dce3a-374">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dce3a-374">Minimum supported server</span></span><br/> | <span data-ttu-id="dce3a-375">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dce3a-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dce3a-376">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dce3a-376">Namespace</span></span><br/>                | <span data-ttu-id="dce3a-377">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dce3a-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dce3a-378">MOF</span><span class="sxs-lookup"><span data-stu-id="dce3a-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dce3a-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dce3a-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dce3a-380">DLL</span><span class="sxs-lookup"><span data-stu-id="dce3a-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dce3a-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dce3a-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dce3a-382">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dce3a-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce3a-383">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="dce3a-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="dce3a-384">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="dce3a-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="dce3a-385">Classes de stockage</span><span class="sxs-lookup"><span data-stu-id="dce3a-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

