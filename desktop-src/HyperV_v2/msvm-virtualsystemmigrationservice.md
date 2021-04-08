---
description: Représente le service de migration de système virtuel. Il est utilisé pour la migration d’un système virtuel ou pour la migration du stockage d’un système virtuel d’une plate-forme de virtualisation vers une autre.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750156"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="35b2f-104">MSVM \_ VirtualSystemMigrationService, classe</span><span class="sxs-lookup"><span data-stu-id="35b2f-104">Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="35b2f-105">Représente le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-105">Represents the virtual system migration service.</span></span> <span data-ttu-id="35b2f-106">Il est utilisé pour la migration d’un système virtuel ou pour la migration du stockage d’un système virtuel d’une plate-forme de virtualisation vers une autre.</span><span class="sxs-lookup"><span data-stu-id="35b2f-106">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span>

<span data-ttu-id="35b2f-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="35b2f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b2f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35b2f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a><span data-ttu-id="35b2f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="35b2f-109">Members</span></span>

<span data-ttu-id="35b2f-110">La classe **MSVM \_ VirtualSystemMigrationService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="35b2f-110">The **Msvm\_VirtualSystemMigrationService** class has these types of members:</span></span>

-   [<span data-ttu-id="35b2f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35b2f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="35b2f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35b2f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="35b2f-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="35b2f-113">Methods</span></span>

<span data-ttu-id="35b2f-114">La classe **MSVM \_ VirtualSystemMigrationService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="35b2f-114">The **Msvm\_VirtualSystemMigrationService** class has these methods.</span></span>



| <span data-ttu-id="35b2f-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="35b2f-115">Method</span></span>                                                                                                                  | <span data-ttu-id="35b2f-116">Description</span><span class="sxs-lookup"><span data-stu-id="35b2f-116">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35b2f-117">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="35b2f-117">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | <span data-ttu-id="35b2f-118">Ajoute les sous-réseaux du réseau de migration pour le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-118">Adds migration network subnets for the virtual system migration service.</span></span><br/>                                                                                          |
| [<span data-ttu-id="35b2f-119">**CheckSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="35b2f-119">**CheckSystemCompatibilityInfo**</span></span>](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="35b2f-120">Vérifie les informations de compatibilité pour la compatibilité avec le système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="35b2f-120">Checks the compatibility information for compatibility with the hosting computer system.</span></span><br/>                                                                          |
| [<span data-ttu-id="35b2f-121">**CheckVirtualSystemIsMigratable**</span><span class="sxs-lookup"><span data-stu-id="35b2f-121">**CheckVirtualSystemIsMigratable**</span></span>](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | <span data-ttu-id="35b2f-122">Méthode permettant de migrer un système virtuel ou le stockage d’un système virtuel vers un ordinateur hôte de destination spécifié par un nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="35b2f-122">Method to migrate a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                              |
| [<span data-ttu-id="35b2f-123">**CheckVirtualSystemIsMigratableToHost**</span><span class="sxs-lookup"><span data-stu-id="35b2f-123">**CheckVirtualSystemIsMigratableToHost**</span></span>](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | <span data-ttu-id="35b2f-124">Détermine si le système virtuel spécifié peut être migré vers un ordinateur hôte cible spécifié par un nom de réseau ou une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="35b2f-124">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span><br/>                                       |
| [<span data-ttu-id="35b2f-125">**GetSystemCompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="35b2f-125">**GetSystemCompatibilityInfo**</span></span>](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="35b2f-126">Génère un blob opaque de données qui contient des informations de compatibilité pour le système spécifié.</span><span class="sxs-lookup"><span data-stu-id="35b2f-126">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span><br/>                                                                |
| [<span data-ttu-id="35b2f-127">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="35b2f-127">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | <span data-ttu-id="35b2f-128">Obtient les vecteurs de compatibilité pour un ordinateur virtuel ou un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="35b2f-128">Gets compatibility vectors for a virtual machine or a host.</span></span><br/> <span data-ttu-id="35b2f-129">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="35b2f-129">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="35b2f-130">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="35b2f-130">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | <span data-ttu-id="35b2f-131">Migre un système virtuel ou le stockage d’un système virtuel vers un ordinateur hôte de destination spécifié par un nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="35b2f-131">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span><br/>                                                       |
| [<span data-ttu-id="35b2f-132">**MigrateVirtualSystemToSystem**</span><span class="sxs-lookup"><span data-stu-id="35b2f-132">**MigrateVirtualSystemToSystem**</span></span>](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | <span data-ttu-id="35b2f-133">Déplace, migre ou déplace un système virtuel vers un système cible.</span><span class="sxs-lookup"><span data-stu-id="35b2f-133">Moves, migrates, or relocates a virtual system to a target system.</span></span><br/>                                                                                                |
| [<span data-ttu-id="35b2f-134">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="35b2f-134">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="35b2f-135">Modifie les sous-réseaux de migration du service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-135">Modifies migration network subnets of the virtual system migration service.</span></span><br/>                                                                                       |
| [<span data-ttu-id="35b2f-136">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="35b2f-136">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="35b2f-137">Modifie les données de paramètre pour le service de migration.</span><span class="sxs-lookup"><span data-stu-id="35b2f-137">Modifies the setting data for the migration service.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="35b2f-138">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="35b2f-138">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | <span data-ttu-id="35b2f-139">Supprime les sous-réseaux du réseau de migration du service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-139">Removes migration network subnets from the virtual system migration service.</span></span><br/>                                                                                      |
| [<span data-ttu-id="35b2f-140">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="35b2f-140">**RequestStateChange**</span></span>](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | <span data-ttu-id="35b2f-141">Demande un changement d’État</span><span class="sxs-lookup"><span data-stu-id="35b2f-141">Requests a state change</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="35b2f-142">**StartService**</span><span class="sxs-lookup"><span data-stu-id="35b2f-142">**StartService**</span></span>](msvm-virtualsystemmigrationservice-startservice.md)                                                 | <span data-ttu-id="35b2f-143">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="35b2f-143">Starts the service.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="35b2f-144">**StopService**</span><span class="sxs-lookup"><span data-stu-id="35b2f-144">**StopService**</span></span>](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | <span data-ttu-id="35b2f-145">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="35b2f-145">Stops the service.</span></span><br/>                                                                                                                                                |



 

### <a name="properties"></a><span data-ttu-id="35b2f-146">Propriétés</span><span class="sxs-lookup"><span data-stu-id="35b2f-146">Properties</span></span>

<span data-ttu-id="35b2f-147">La classe **MSVM \_ VirtualSystemMigrationService** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="35b2f-147">The **Msvm\_VirtualSystemMigrationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35b2f-148">**ActiveStorageMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="35b2f-148">**ActiveStorageMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35b2f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-151">Nombre de migrations de stockage actuelles en cours.</span><span class="sxs-lookup"><span data-stu-id="35b2f-151">The number of current storage migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-152">**ActiveVirtualSystemMigrationCount**</span><span class="sxs-lookup"><span data-stu-id="35b2f-152">**ActiveVirtualSystemMigrationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-153">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35b2f-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-155">Nombre de migrations actuelles du système virtuel en cours.</span><span class="sxs-lookup"><span data-stu-id="35b2f-155">The number of current virtual system migrations in progress.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="35b2f-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-157">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-159">Indique les valeurs possibles pour le paramètre *RequestedState* de la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="35b2f-159">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="35b2f-160">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35b2f-160">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="35b2f-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-164">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35b2f-164">A short description of the object.</span></span> <span data-ttu-id="35b2f-165">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de migration Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-166">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="35b2f-166">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-169">Indique la capacité de l’instrumentation à communiquer avec l’élément managé sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="35b2f-169">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="35b2f-170">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35b2f-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35b2f-171">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35b2f-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35b2f-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-175">Nom de la classe ou de la sous-classe utilisée dans la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="35b2f-175">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="35b2f-176">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ VirtualSystemMigrationService ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-176">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemMigrationService".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-177">**Description**</span><span class="sxs-lookup"><span data-stu-id="35b2f-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-180">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="35b2f-180">A description of the object.</span></span> <span data-ttu-id="35b2f-181">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de migration Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-182">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="35b2f-182">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-183">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-185">Complète la propriété **PrimaryStatus** avec des détails d’État supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="35b2f-185">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="35b2f-186">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35b2f-186">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35b2f-187">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35b2f-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-188">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="35b2f-188">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-191">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35b2f-191">A display name for the object.</span></span> <span data-ttu-id="35b2f-192">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « service de migration Hyper-V ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Migration Service".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-193">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="35b2f-193">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-194">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-196">Configuration par défaut ou de démarrage d’un administrateur pour l’état activé d’un élément.</span><span class="sxs-lookup"><span data-stu-id="35b2f-196">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="35b2f-197">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="35b2f-197">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-198">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="35b2f-198">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-201">États activés et désactivés d’un élément.</span><span class="sxs-lookup"><span data-stu-id="35b2f-201">The enabled and disabled states of an element.</span></span> <span data-ttu-id="35b2f-202">Cette propriété peut également indiquer les transitions entre ces États demandés.</span><span class="sxs-lookup"><span data-stu-id="35b2f-202">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="35b2f-203">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur 2 (activé).</span><span class="sxs-lookup"><span data-stu-id="35b2f-203">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-204">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="35b2f-204">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-205">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-207">Intégrité actuelle de l’élément.</span><span class="sxs-lookup"><span data-stu-id="35b2f-207">The current health of the element.</span></span> <span data-ttu-id="35b2f-208">Cet attribut exprime l’intégrité de cet élément, mais pas nécessairement celle de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="35b2f-208">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="35b2f-209">Les valeurs possibles sont comprises entre 0 et 30, où 5 signifie que l’élément est entièrement sain et 30 signifie que l’élément est complètement non opérationnel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-209">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="35b2f-210">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="35b2f-210">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35b2f-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-212">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35b2f-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-214">Date et heure de création de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-214">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="35b2f-215">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35b2f-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-216">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35b2f-216">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-219">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="35b2f-219">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-220">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="35b2f-220">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="35b2f-221">Cette propriété est héritée de [**CIM \_ propriété ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35b2f-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-222">**MigrationServiceListenerIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="35b2f-222">**MigrationServiceListenerIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-223">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="35b2f-223">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-225">Liste des adresses IP de l’hôte qui peuvent être utilisées pour la migration du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="35b2f-225">The list of host IP addresses that can be used for virtual system migration.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-226">**Nom**</span><span class="sxs-lookup"><span data-stu-id="35b2f-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-229">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="35b2f-229">The label by which the object is known.</span></span> <span data-ttu-id="35b2f-230">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « migrationwmi ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-230">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "migrationwmi".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-231">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="35b2f-231">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-232">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-234">Fournit des informations sur l’état actuel de la condition opérationnelle de l’élément et peut être utilisé pour fournir plus de détails concernant la valeur de la propriété **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="35b2f-234">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="35b2f-235">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35b2f-235">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35b2f-236">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35b2f-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-237">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="35b2f-237">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-238">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-238">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-239">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-240">États actuels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="35b2f-240">The current statuses of the object.</span></span> <span data-ttu-id="35b2f-241">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau a toujours la valeur 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="35b2f-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-242">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="35b2f-242">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-244">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-245">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1 (autre).</span><span class="sxs-lookup"><span data-stu-id="35b2f-245">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="35b2f-246">Cette propriété doit avoir la valeur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="35b2f-246">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="35b2f-247">Cette propriété est héritée de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35b2f-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-248">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="35b2f-248">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-251">Valeur qui fournit des informations sur la façon dont le propriétaire principal du service est accessible (par exemple, numéro de téléphone, adresse e-mail, etc.).</span><span class="sxs-lookup"><span data-stu-id="35b2f-251">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="35b2f-252">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35b2f-252">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-253">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="35b2f-253">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-256">Nom du propriétaire principal du service, s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="35b2f-256">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="35b2f-257">Le propriétaire principal est le contact de support initial pour le service.</span><span class="sxs-lookup"><span data-stu-id="35b2f-257">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="35b2f-258">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35b2f-258">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-259">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="35b2f-259">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-260">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-261">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-262">Fournit des informations d’état de haut niveau.</span><span class="sxs-lookup"><span data-stu-id="35b2f-262">Provides high level status information.</span></span> <span data-ttu-id="35b2f-263">Cette propriété doit être utilisée conjointement avec la propriété **DetailedStatus** pour fournir un état d’intégrité élevé et détaillé de l’élément et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="35b2f-263">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="35b2f-264">Une valeur **null** indique que cette propriété n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="35b2f-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="35b2f-265">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="35b2f-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-266">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="35b2f-266">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-267">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-269">Dernier État demandé ou souhaité pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="35b2f-269">The last requested or desired state for the element.</span></span> <span data-ttu-id="35b2f-270">L’état réel de l’élément est représenté par **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="35b2f-270">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="35b2f-271">Cette propriété est fournie pour comparer les derniers États activés et actuellement activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="35b2f-271">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="35b2f-272">Une instance particulière de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) peut ne pas prendre en charge la méthode **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="35b2f-272">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="35b2f-273">Si cela se produit, la valeur 12 (non applicable) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="35b2f-273">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="35b2f-274">Cette propriété est héritée de la **\_ EnabledLogicalElement CIM** et est toujours définie sur 12 (non applicable).</span><span class="sxs-lookup"><span data-stu-id="35b2f-274">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-275">**Cours**</span><span class="sxs-lookup"><span data-stu-id="35b2f-275">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-276">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="35b2f-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-278">Indique si le service est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="35b2f-278">Indicates whether the service is currently running.</span></span> <span data-ttu-id="35b2f-279">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="35b2f-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-280">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="35b2f-280">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-281">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-283">Valeur de chaîne qui indique si le service est démarré automatiquement par un système, un système d’exploitation ou s’il est démarré uniquement sur demande.</span><span class="sxs-lookup"><span data-stu-id="35b2f-283">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="35b2f-284">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur **null**.</span><span class="sxs-lookup"><span data-stu-id="35b2f-284">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-285">**État**</span><span class="sxs-lookup"><span data-stu-id="35b2f-285">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-288">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et est toujours définie sur « OK ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-289">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="35b2f-289">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-290">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="35b2f-290">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-292">Chaînes qui décrivent les différentes valeurs de tableau **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="35b2f-292">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="35b2f-293">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)et les chaînes ont toujours la valeur « OK ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-293">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-294">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35b2f-294">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-296">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-297">Nom de la classe de création du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="35b2f-297">The scoping system's creation class name.</span></span> <span data-ttu-id="35b2f-298">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service)et est toujours définie sur « MSVM \_ ComputerSystem ».</span><span class="sxs-lookup"><span data-stu-id="35b2f-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-299">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="35b2f-299">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="35b2f-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-302">Nom du système de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="35b2f-302">The name of the hosting computer system.</span></span> <span data-ttu-id="35b2f-303">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="35b2f-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-304">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="35b2f-304">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-305">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35b2f-305">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-307">Date ou heure de la dernière modification de l’état activé de l’élément.</span><span class="sxs-lookup"><span data-stu-id="35b2f-307">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="35b2f-308">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35b2f-308">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="35b2f-309">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="35b2f-309">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35b2f-310">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35b2f-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35b2f-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="35b2f-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35b2f-312">Indique l’État cible de la transition de l’instance.</span><span class="sxs-lookup"><span data-stu-id="35b2f-312">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="35b2f-313">Cette propriété est héritée de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="35b2f-313">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35b2f-314">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35b2f-314">Requirements</span></span>



| <span data-ttu-id="35b2f-315">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35b2f-315">Requirement</span></span> | <span data-ttu-id="35b2f-316">Valeur</span><span class="sxs-lookup"><span data-stu-id="35b2f-316">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b2f-317">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35b2f-317">Minimum supported client</span></span><br/> | <span data-ttu-id="35b2f-318">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35b2f-318">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35b2f-319">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35b2f-319">Minimum supported server</span></span><br/> | <span data-ttu-id="35b2f-320">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35b2f-320">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35b2f-321">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35b2f-321">Namespace</span></span><br/>                | <span data-ttu-id="35b2f-322">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="35b2f-322">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35b2f-323">MOF</span><span class="sxs-lookup"><span data-stu-id="35b2f-323">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35b2f-324"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35b2f-324"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35b2f-325">DLL</span><span class="sxs-lookup"><span data-stu-id="35b2f-325">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35b2f-326"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35b2f-326"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

