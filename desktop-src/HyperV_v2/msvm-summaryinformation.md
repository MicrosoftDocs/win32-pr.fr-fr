---
description: Utilisé dans les méthodes GetSummaryInformation et GetDefinitionFileSummaryInformation de la \_ classe MSVM VirtualSystemManagementService pour récupérer rapidement les informations communes relatives à un ordinateur virtuel ou à un instantané.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Classe Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515882"
---
# <a name="msvm_summaryinformation-class"></a><span data-ttu-id="66bbc-103">MSVM \_ SummaryInformation, classe</span><span class="sxs-lookup"><span data-stu-id="66bbc-103">Msvm\_SummaryInformation class</span></span>

<span data-ttu-id="66bbc-104">Utilisé dans les méthodes [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) et [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pour récupérer rapidement les informations communes relatives à un ordinateur virtuel ou à un instantané.</span><span class="sxs-lookup"><span data-stu-id="66bbc-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) and [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) methods in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual machine or snapshot.</span></span>

<span data-ttu-id="66bbc-105">La syntaxe suivante est simplifiée format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="66bbc-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bbc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66bbc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="66bbc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="66bbc-107">Members</span></span>

<span data-ttu-id="66bbc-108">La classe **MSVM \_ SummaryInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="66bbc-108">The **Msvm\_SummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="66bbc-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66bbc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66bbc-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="66bbc-110">Properties</span></span>

<span data-ttu-id="66bbc-111">La classe **MSVM \_ SummaryInformation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="66bbc-111">The **Msvm\_SummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66bbc-112">**AllocatedGPU**</span><span class="sxs-lookup"><span data-stu-id="66bbc-112">**AllocatedGPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-115">Identificateur de l’unité de traitement graphique (GPU) physique allouée à cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-115">The identifier of the physical graphics processing unit (GPU) allocated to this virtual machine.</span></span> <span data-ttu-id="66bbc-116">Cette propriété s’applique uniquement aux machines virtuelles qui utilisent RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="66bbc-116">This property only applies to virtual machines that use RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-117">**ApplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="66bbc-117">**ApplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-118">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-120">État d’intégrité actuel de l’application pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-120">The current application health status for the virtual machine.</span></span> <span data-ttu-id="66bbc-121">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-121">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="66bbc-122">**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-122">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

<span data-ttu-id="66bbc-123">**Critique** pour l’Application (32782)</span><span class="sxs-lookup"><span data-stu-id="66bbc-123">**Application Critical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66bbc-124">**Désactivé** (32896)</span><span class="sxs-lookup"><span data-stu-id="66bbc-124">**Disabled** (32896)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-125">**AsynchronousTasks**</span><span class="sxs-lookup"><span data-stu-id="66bbc-125">**AsynchronousTasks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-126">Type de données : tableau **\_ ConcreteJob CIM**</span><span class="sxs-lookup"><span data-stu-id="66bbc-126">Data type: **CIM\_ConcreteJob** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-128">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-129">Tableau d’instances [**MSVM \_ ConcreteJob**](msvm-concretejob.md) qui représentent les opérations asynchrones relatives à l’ordinateur virtuel en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="66bbc-129">An array of [**Msvm\_ConcreteJob**](msvm-concretejob.md) instances that represent any asynchronous operations related to the virtual machine that are currently executing.</span></span> <span data-ttu-id="66bbc-130">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-130">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-131">**AvailableMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="66bbc-131">**AvailableMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="66bbc-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-134">Pourcentage de mémoire tampon disponible pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-134">The percentage of available memory buffer for the virtual machine.</span></span> <span data-ttu-id="66bbc-135">Lorsque la mémoire dynamique est activée pour un ordinateur virtuel, cette propriété représente le rapport entre la mémoire tampon disponible et la mémoire tampon idéale pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-135">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory buffer to the ideal memory buffer for the virtual machine.</span></span> <span data-ttu-id="66bbc-136">La taille de mémoire tampon idéale est configurée à l’aide de la propriété **TargetMemoryBuffer** de la classe [**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-136">The ideal memory buffer size is configured by using the **TargetMemoryBuffer** property of the [**Msvm\_MemorySettingData**](msvm-memorysettingdata.md) class.</span></span>

<span data-ttu-id="66bbc-137">Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent des ordinateurs virtuels pour lesquels la mémoire dynamique n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="66bbc-137">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="66bbc-138">Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-138">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-139">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="66bbc-139">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-140">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66bbc-140">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-142">Heure de création de l’ordinateur virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="66bbc-142">The time at which the virtual machine or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="66bbc-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-146">Nom complet de l’ordinateur virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="66bbc-146">The display name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-147">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="66bbc-147">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-148">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-150">État actuel de l’ordinateur virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="66bbc-150">The current state of the virtual machine or snapshot.</span></span> <span data-ttu-id="66bbc-151">Pour connaître les valeurs possibles, consultez la propriété **EnabledState** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-151">See the **EnabledState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-152">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="66bbc-152">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-153">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-155">Indique si les connexions en mode étendu sont autorisées par l’hôte et, si elles sont autorisées, si elles sont disponibles pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-155">Indicates whether enhanced mode connections are allowed by the host, and if allowed, whether they are available to the virtual machine.</span></span>

<span data-ttu-id="66bbc-156">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="66bbc-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="66bbc-157">**Autorisé et disponible** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-157">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="66bbc-158">**Non autorisé** (3)</span><span class="sxs-lookup"><span data-stu-id="66bbc-158">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="66bbc-159">**Autorisé mais non disponible** (6)</span><span class="sxs-lookup"><span data-stu-id="66bbc-159">**Allowed but not available** (6 )</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-160">**GuestOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="66bbc-160">**GuestOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-163">Nom du système d’exploitation invité, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="66bbc-163">The name of the guest operating system, if available.</span></span> <span data-ttu-id="66bbc-164">Si ces informations ne sont pas disponibles, la valeur de cette propriété est **null**.</span><span class="sxs-lookup"><span data-stu-id="66bbc-164">If this information is not available, the value of this property is **Null**.</span></span> <span data-ttu-id="66bbc-165">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-165">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-166">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="66bbc-166">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-169">État d’intégrité actuel de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-169">The current health state for the virtual machine.</span></span> <span data-ttu-id="66bbc-170">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-170">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-171">**Pulsation**</span><span class="sxs-lookup"><span data-stu-id="66bbc-171">**Heartbeat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-172">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-174">État actuel de la pulsation pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-174">The current heartbeat status for the virtual machine.</span></span> <span data-ttu-id="66bbc-175">Pour plus d’informations, consultez la documentation relative à la propriété [**StatusDescriptions**](msvm-heartbeatcomponent.md) de la classe **\_ HeartbeatComponent MSVM** .</span><span class="sxs-lookup"><span data-stu-id="66bbc-175">For more information, see the documentation for the [**StatusDescriptions**](msvm-heartbeatcomponent.md) property of the **Msvm\_HeartbeatComponent** class.</span></span> <span data-ttu-id="66bbc-176">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-176">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

<dl> <dt>

<span data-ttu-id="66bbc-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-177"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erreur** (6)</span><span class="sxs-lookup"><span data-stu-id="66bbc-178"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Aucun contact** (12)</span><span class="sxs-lookup"><span data-stu-id="66bbc-179"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Perte de communication** (13)</span><span class="sxs-lookup"><span data-stu-id="66bbc-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-181">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="66bbc-181">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-184">Nom de l’ordinateur hébergeant cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-184">The name of the computer hosting this virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-185">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66bbc-185">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="66bbc-186">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="66bbc-186">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-189">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ propriété ManagedElement. InstanceId"), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="66bbc-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-190">InstanceID est une propriété facultative qui peut être utilisée pour identifier de manière opaque et unique une instance de cette classe dans l’étendue de l’espace de noms d’instanciation.</span><span class="sxs-lookup"><span data-stu-id="66bbc-190">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="66bbc-191">Plusieurs sous-classes de cette classe peuvent substituer cette propriété pour la rendre obligatoire ou une clé.</span><span class="sxs-lookup"><span data-stu-id="66bbc-191">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="66bbc-192">Ces sous-classes peuvent également modifier les algorithmes préférés pour garantir l’unicité définie ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="66bbc-192">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="66bbc-193">Pour garantir l’unicité dans l’espace de noms, la valeur d’InstanceID doit être construite à l’aide de l’algorithme « préféré » suivant :</span><span class="sxs-lookup"><span data-stu-id="66bbc-193">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="66bbc-194"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="66bbc-194"><OrgID>:<LocalID></span></span>

<span data-ttu-id="66bbc-195">Où <OrgID> et <LocalID> sont séparés par un signe deux-points ( :), et où <OrgID> doivent inclure un nom protégé par des droits d’auteur, une marque ou un nom unique qui est détenu par l’entité commerciale qui crée ou définit l’InstanceId ou qui est un ID inscrit affecté à l’entité métier par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="66bbc-195">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="66bbc-196">(Cette spécification est semblable à la <Schema Name> \_ <Class Name> suivante : structure des noms de classes de schéma.) En outre, pour garantir l’unicité, <OrgID> ne doit pas contenir de deux-points ( :).</span><span class="sxs-lookup"><span data-stu-id="66bbc-196">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="66bbc-197">Lors de l’utilisation de cet algorithme, le premier signe deux-points devant apparaître dans InstanceID doit apparaître entre <OrgID> et <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="66bbc-197">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="66bbc-198"><LocalID> est choisi par l’entité métier et ne doit pas être réutilisé pour identifier les différents éléments sous-jacents (réels).</span><span class="sxs-lookup"><span data-stu-id="66bbc-198"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="66bbc-199">Si la valeur n’est pas null et que l’algorithme « préféré » ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que l’InstanceID qui en résulte n’est pas réutilisé dans les InstanceIDs produits par ce ou d’autres fournisseurs pour l’espace de noms de cette instance.</span><span class="sxs-lookup"><span data-stu-id="66bbc-199">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="66bbc-200">Si vous ne définissez pas la valeur null pour les instances définies par DMTF, l’algorithme « préféré » doit être utilisé avec le <OrgID> défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="66bbc-200">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-201">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66bbc-201">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="66bbc-202">**IntegrationServicesVersionState**</span><span class="sxs-lookup"><span data-stu-id="66bbc-202">**IntegrationServicesVersionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-203">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-205">Indique si les services d’intégration installés sur l’ordinateur virtuel sont à jour.</span><span class="sxs-lookup"><span data-stu-id="66bbc-205">Indicates whether the integration services installed in the virtual machine are up to date.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66bbc-206">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="66bbc-206">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

<span data-ttu-id="66bbc-207">**Uptodate** (1)</span><span class="sxs-lookup"><span data-stu-id="66bbc-207">**UpToDate** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

<span data-ttu-id="66bbc-208">**Incompatibilité** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-208">**Mismatch** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-209">**MemoryAvailable**</span><span class="sxs-lookup"><span data-stu-id="66bbc-209">**MemoryAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="66bbc-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-212">Pourcentage de la mémoire actuelle disponible pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-212">The percentage of the current memory available to the virtual machine.</span></span> <span data-ttu-id="66bbc-213">Lorsque la mémoire dynamique est activée pour un ordinateur virtuel, cette propriété représente le rapport entre la mémoire disponible de l’ordinateur virtuel et la mémoire physique totale affectée à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-213">When dynamic memory is enabled for a virtual machine, this property represents the ratio of available memory of the virtual machine to the total physical memory assigned to the virtual machine.</span></span> <span data-ttu-id="66bbc-214">Lorsqu’un ordinateur virtuel n’a pas de mémoire disponible, cette propriété est négative et contient le ratio de mémoire nécessaire pour l’ordinateur virtuel à la mémoire physique totale affectée à l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-214">When a virtual machine has no available memory, this property will be negative, and it will contain the ratio of memory needed for the virtual machine to the total physical memory assigned to the virtual machine.</span></span>

<span data-ttu-id="66bbc-215">Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent des ordinateurs virtuels pour lesquels la mémoire dynamique n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="66bbc-215">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent virtual machines for which dynamic memory is not enabled.</span></span>

<span data-ttu-id="66bbc-216">Cette propriété n’est pas valide pour les instances de la classe **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-216">This property is not valid for instances of the **Msvm\_SummaryInformation** class that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-217">**MemorySpansPhysicalNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="66bbc-217">**MemorySpansPhysicalNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-218">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="66bbc-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-220">Indique si la mémoire de l’un ou plusieurs des nœuds NUMA (non-Uniform Memory Access) virtuels de l’ordinateur virtuel s’étend sur plusieurs nœuds NUMA physiques du système informatique d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="66bbc-220">Indicates whether the memory of the one or more of the virtual nonuniform memory access (NUMA) nodes of the virtual machine spans multiple physical NUMA nodes of the hosting computer system.</span></span> <span data-ttu-id="66bbc-221">Contient la **valeur true** si la mémoire s’étend sur plusieurs nœuds NUMA physiques ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="66bbc-221">Contains **True** if the memory spans multiple physical NUMA nodes or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-222">**MemoryUsage**</span><span class="sxs-lookup"><span data-stu-id="66bbc-222">**MemoryUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-223">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66bbc-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-225">Utilisation actuelle de la mémoire, en mégaoctets, de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-225">The current memory usage, in megabytes, of the virtual machine.</span></span> <span data-ttu-id="66bbc-226">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-226">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-227">**Nom**</span><span class="sxs-lookup"><span data-stu-id="66bbc-227">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-229">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-230">Nom unique de l’ordinateur virtuel ou de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="66bbc-230">The unique name for the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-231">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="66bbc-231">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-234">Remarques associées à la machine virtuelle ou à la capture instantanée.</span><span class="sxs-lookup"><span data-stu-id="66bbc-234">The notes associated with the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-235">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="66bbc-235">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-236">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-237">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-238">Nombre total de processeurs virtuels alloués à l’ordinateur virtuel ou à la capture instantanée.</span><span class="sxs-lookup"><span data-stu-id="66bbc-238">The total number of virtual processors allocated to the virtual machine or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-239">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="66bbc-239">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-240">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-241">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-242">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-242">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-243">États opérationnels actuels de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-243">The current operational statuses of the virtual machine.</span></span> <span data-ttu-id="66bbc-244">Pour connaître les valeurs possibles, consultez la propriété **OperationalStatus** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-244">See the **OperationalStatus** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-245">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="66bbc-245">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-247">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-248">Chaîne qui décrit l’état activé ou désactivé de l’élément lorsque la propriété **EnabledState** a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="66bbc-248">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1.</span></span> <span data-ttu-id="66bbc-249">Cette propriété est définie sur **null** quand **EnabledState** a une valeur autre que 1.</span><span class="sxs-lookup"><span data-stu-id="66bbc-249">This property will be set to **Null** when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-250">**ProcessorLoad**</span><span class="sxs-lookup"><span data-stu-id="66bbc-250">**ProcessorLoad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-251">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-253">Utilisation actuelle du processeur de l’ordinateur virtuel, en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="66bbc-253">The current processor usage of the virtual machine, in percentage.</span></span> <span data-ttu-id="66bbc-254">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-254">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-255">**ProcessorLoadHistory**</span><span class="sxs-lookup"><span data-stu-id="66bbc-255">**ProcessorLoadHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-256">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-258">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-258">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-259">Tableau des précédents exemples 100 de l’utilisation du processeur, en pourcentage, pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-259">An array of the previous 100 samples of the processor usage, in percentage, for the virtual machine.</span></span> <span data-ttu-id="66bbc-260">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-260">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-261">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="66bbc-261">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-262">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-264">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationHealthEx**")</span><span class="sxs-lookup"><span data-stu-id="66bbc-264">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationHealthEx**")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-265">Intégrité de la réplication pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-265">The replication health for the virtual machine.</span></span> <span data-ttu-id="66bbc-266">Pour connaître les valeurs possibles, consultez la propriété **ReplicationHealth** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-266">See the **ReplicationHealth** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-267">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt **ReplicationHealthEx**.</span><span class="sxs-lookup"><span data-stu-id="66bbc-267">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationHealthEx**.</span></span>

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="66bbc-268">**Non applicable** (0)</span><span class="sxs-lookup"><span data-stu-id="66bbc-268">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="66bbc-269">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="66bbc-269">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="66bbc-270">**Avertissement** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-270">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="66bbc-271">**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="66bbc-271">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-272">**ReplicationHealthEx**</span><span class="sxs-lookup"><span data-stu-id="66bbc-272">**ReplicationHealthEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-273">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-275">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-275">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-276">Tableau des valeurs d’intégrité de la réplication pour les différentes relations de réplication de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-276">The array of replication health values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="66bbc-277">Pour connaître les valeurs possibles, consultez la propriété **ReplicationHealth** de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-277">See the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="66bbc-278">**Non applicable** (0)</span><span class="sxs-lookup"><span data-stu-id="66bbc-278">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="66bbc-279">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="66bbc-279">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="66bbc-280">**Avertissement** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-280">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="66bbc-281">**Critique** (3)</span><span class="sxs-lookup"><span data-stu-id="66bbc-281">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-282">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="66bbc-282">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-283">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-285">Type de réplication pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-285">The replication type for the virtual machine.</span></span> <span data-ttu-id="66bbc-286">Pour connaître les valeurs possibles, consultez la propriété **ReplicationMode** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-286">See the **ReplicationMode** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="66bbc-287">**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="66bbc-287">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="66bbc-288">**Principal** (1)</span><span class="sxs-lookup"><span data-stu-id="66bbc-288">**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="66bbc-289">**Réplica** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-289">**Replica** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="66bbc-290">**Réplica de test** (3)</span><span class="sxs-lookup"><span data-stu-id="66bbc-290">**Test Replica** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="66bbc-291">**Réplica étendu** (4)</span><span class="sxs-lookup"><span data-stu-id="66bbc-291">**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-292">**ReplicationProviderId**</span><span class="sxs-lookup"><span data-stu-id="66bbc-292">**ReplicationProviderId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-293">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="66bbc-293">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-295">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-295">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-296">Pour la machine virtuelle de réplication principale ou étendue, il s’agit de l’ID du fournisseur de réplication principal.</span><span class="sxs-lookup"><span data-stu-id="66bbc-296">For the primary or extended replica virtual machine, this is the primary replication provider ID.</span></span> <span data-ttu-id="66bbc-297">Pour un ordinateur virtuel de réplication et si la réplication étendue est activée, il s’agit de l’ID de fournisseur pour la relation étendue.</span><span class="sxs-lookup"><span data-stu-id="66bbc-297">For a replica virtual machine and if extended replication is enabled, this is the provider ID for extended relationship.</span></span>

<span data-ttu-id="66bbc-298">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="66bbc-298">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-299">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="66bbc-299">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-300">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-302">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**MSVM \_ SummaryInformation**.**ReplicationStateEx**")</span><span class="sxs-lookup"><span data-stu-id="66bbc-302">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm\_SummaryInformation**.**ReplicationStateEx**")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-303">État de réplication de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-303">The replication state for the virtual machine.</span></span> <span data-ttu-id="66bbc-304">Pour connaître les valeurs possibles, consultez la propriété **ReplicationState** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-304">See the **ReplicationState** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for possible values.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-305">Cette propriété est déconseillée à partir de Windows 8.1 ; Utilisez plutôt **ReplicationStateEx**.</span><span class="sxs-lookup"><span data-stu-id="66bbc-305">This property is deprecated starting with Windows 8.1; instead, use the **ReplicationStateEx**.</span></span>

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66bbc-306">**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="66bbc-306">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="66bbc-307">**Prêt pour la réplication** (1)</span><span class="sxs-lookup"><span data-stu-id="66bbc-307">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="66bbc-308">**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-308">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="66bbc-309">**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="66bbc-309">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="66bbc-310">**Réplication synchronisée terminée** (4)</span><span class="sxs-lookup"><span data-stu-id="66bbc-310">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="66bbc-311">**Récupéré** (5)</span><span class="sxs-lookup"><span data-stu-id="66bbc-311">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="66bbc-312">**Validé** (6)</span><span class="sxs-lookup"><span data-stu-id="66bbc-312">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="66bbc-313">**Suspendu** (7)</span><span class="sxs-lookup"><span data-stu-id="66bbc-313">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="66bbc-314">**Critique** (8)</span><span class="sxs-lookup"><span data-stu-id="66bbc-314">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="66bbc-315">**En attente de démarrage de la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="66bbc-315">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="66bbc-316">**Resynchronisation** (10)</span><span class="sxs-lookup"><span data-stu-id="66bbc-316">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="66bbc-317">**Resynchronisation suspendue** (11)</span><span class="sxs-lookup"><span data-stu-id="66bbc-317">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="66bbc-318">**Basculement en cours** (12)</span><span class="sxs-lookup"><span data-stu-id="66bbc-318">**Failover in progress** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-319">**ReplicationStateEx**</span><span class="sxs-lookup"><span data-stu-id="66bbc-319">**ReplicationStateEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-320">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-321">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-322">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-322">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-323">Tableau des valeurs d’état de réplication pour les différentes relations de réplication de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-323">The array of replication state values for the various replication relationships of the virtual machine.</span></span> <span data-ttu-id="66bbc-324">Pour connaître les valeurs possibles, consultez la propriété **ReplicationState** de la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-324">See the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class for possible values.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66bbc-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="66bbc-325"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="66bbc-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Prêt pour la réplication** (1)</span><span class="sxs-lookup"><span data-stu-id="66bbc-326"><span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="66bbc-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**En attente de l’exécution de la réplication initiale** (2)</span><span class="sxs-lookup"><span data-stu-id="66bbc-327"><span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="66bbc-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Réplication** (3)</span><span class="sxs-lookup"><span data-stu-id="66bbc-328"><span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="66bbc-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Réplication synchronisée terminée** (4)</span><span class="sxs-lookup"><span data-stu-id="66bbc-329"><span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="66bbc-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Récupéré** (5)</span><span class="sxs-lookup"><span data-stu-id="66bbc-330"><span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="66bbc-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Validé** (6)</span><span class="sxs-lookup"><span data-stu-id="66bbc-331"><span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="66bbc-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendu** (7)</span><span class="sxs-lookup"><span data-stu-id="66bbc-332"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="66bbc-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (8)</span><span class="sxs-lookup"><span data-stu-id="66bbc-333"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="66bbc-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**En attente de démarrage de la resynchronisation** (9)</span><span class="sxs-lookup"><span data-stu-id="66bbc-334"><span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="66bbc-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronisation** (10)</span><span class="sxs-lookup"><span data-stu-id="66bbc-335"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="66bbc-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronisation suspendue** (11)</span><span class="sxs-lookup"><span data-stu-id="66bbc-336"><span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="66bbc-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Basculement en cours** (12)</span><span class="sxs-lookup"><span data-stu-id="66bbc-337"><span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="66bbc-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Restauration automatique en cours** (13)</span><span class="sxs-lookup"><span data-stu-id="66bbc-338"><span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="66bbc-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Restauration automatique terminée** (14)</span><span class="sxs-lookup"><span data-stu-id="66bbc-339"><span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback complete** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span data-ttu-id="66bbc-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Mise à jour du disque en cours** (15)</span><span class="sxs-lookup"><span data-stu-id="66bbc-340"><span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Disk update in progress** (15)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-341">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-341">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span data-ttu-id="66bbc-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Mise à jour critique du disque** (16)</span><span class="sxs-lookup"><span data-stu-id="66bbc-342"><span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Disk update critical** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-343">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-343">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66bbc-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (17)</span><span class="sxs-lookup"><span data-stu-id="66bbc-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (17)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-345">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-345">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="66bbc-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Réplication réaffectée en cours** (18)</span><span class="sxs-lookup"><span data-stu-id="66bbc-346"><span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Repurpose replication in progress** (18)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-347">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-347">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span data-ttu-id="66bbc-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Préparation pour la réplication de la synchronisation** (19)</span><span class="sxs-lookup"><span data-stu-id="66bbc-348"><span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Prepared for sync replication** (19)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-349">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-349">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span data-ttu-id="66bbc-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Préparé pour la réplication inverse de groupe** (20)</span><span class="sxs-lookup"><span data-stu-id="66bbc-350"><span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Prepared for group reverse replication** (20)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-351">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-351">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span data-ttu-id="66bbc-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill en cours** (21)</span><span class="sxs-lookup"><span data-stu-id="66bbc-352"><span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in progress** (21)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="66bbc-353">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-353">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66bbc-354">**Protégé**</span><span class="sxs-lookup"><span data-stu-id="66bbc-354">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-355">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="66bbc-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-356">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-357">Indique si la protection est configurée pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-357">Indicates whether or not shielding is configured for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-358">Ajouté dans Windows 10, version 1703 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="66bbc-358">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="66bbc-359">**Instantanés**</span><span class="sxs-lookup"><span data-stu-id="66bbc-359">**Snapshots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-360">Type de données : tableau **\_ VirtualSystemSettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="66bbc-360">Data type: **CIM\_VirtualSystemSettingData** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-362">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-362">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-363">Tableau d’instances [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) qui représentent les instantanés de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-363">An array of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances that represent the snapshots for the virtual machine.</span></span> <span data-ttu-id="66bbc-364">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-364">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-365">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="66bbc-365">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-366">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="66bbc-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-367">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-368">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-368">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-369">Chaînes qui décrivent les valeurs de tableau **OperationalStatus** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="66bbc-369">Strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="66bbc-370">Cela correspond à la propriété **StatusDescriptions** de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="66bbc-370">This corresponds to the **StatusDescriptions** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-371">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="66bbc-371">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-372">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="66bbc-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-373">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-374">Indique si la pagination de second niveau est active.</span><span class="sxs-lookup"><span data-stu-id="66bbc-374">Indicates whether second level paging is active.</span></span> <span data-ttu-id="66bbc-375">Contient la **valeur true** si la pagination de second niveau est active ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="66bbc-375">Contains **True** if second level paging is active or **False** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-376">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="66bbc-376">**TestReplicaSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-377">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="66bbc-377">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-379">Référence à une [**instance \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel de réplication de test pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-379">Reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the test replica virtual machine for the virtual machine.</span></span> <span data-ttu-id="66bbc-380">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-380">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-381">**ThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="66bbc-381">**ThumbnailImage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-382">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="66bbc-382">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-383">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-384">Qualificateurs : **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImageWidth**","**MSVM \_ SummaryInformation**.**ThumbnailImageHeight**")</span><span class="sxs-lookup"><span data-stu-id="66bbc-384">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImageWidth**", "**Msvm\_SummaryInformation**.**ThumbnailImageHeight**")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-385">Tableau qui contient une petite image de taille miniature du Bureau de l’ordinateur virtuel ou de l’instantané au format RGB565.</span><span class="sxs-lookup"><span data-stu-id="66bbc-385">An array that contains a small, thumbnail-sized image of the desktop for the virtual machine or snapshot in RGB565 format.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-386">**ThumbnailImageHeight**</span><span class="sxs-lookup"><span data-stu-id="66bbc-386">**ThumbnailImageHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-387">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-389">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="66bbc-389">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-390">Hauteur, en pixels, de l’image dans la propriété ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="66bbc-390">The height in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-391">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66bbc-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="66bbc-392">**ThumbnailImageWidth**</span><span class="sxs-lookup"><span data-stu-id="66bbc-392">**ThumbnailImageWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-393">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66bbc-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-394">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-395">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**MSVM \_ SummaryInformation**.**ThumbnailImage**")</span><span class="sxs-lookup"><span data-stu-id="66bbc-395">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm\_SummaryInformation**.**ThumbnailImage**")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-396">Largeur en pixels de l’image dans la propriété ThumbnailImage.</span><span class="sxs-lookup"><span data-stu-id="66bbc-396">The width in pixels of the image in the ThumbnailImage property.</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-397">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66bbc-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="66bbc-398">**Activité**</span><span class="sxs-lookup"><span data-stu-id="66bbc-398">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-399">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66bbc-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-401">Durée écoulée depuis le dernier démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66bbc-401">The amount of time since the virtual machine was last booted.</span></span> <span data-ttu-id="66bbc-402">Cette propriété n’est pas valide pour les instances de **MSVM \_ SummaryInformation** qui représentent un instantané d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-402">This property is not valid for instances of **Msvm\_SummaryInformation** that represent a virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-403">**Version**</span><span class="sxs-lookup"><span data-stu-id="66bbc-403">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-404">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-406">Version du système virtuel dans un format « major. minor », par exemple « 2,0 ».</span><span class="sxs-lookup"><span data-stu-id="66bbc-406">The version of the virtual system in a format of "major.minor", for example "2.0".</span></span>

> [!Note]  
> <span data-ttu-id="66bbc-407">Ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="66bbc-407">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="66bbc-408">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="66bbc-408">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-409">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="66bbc-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-410">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-411">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="66bbc-411">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-412">Chaînes qui spécifient les noms conviviaux des commutateurs virtuels auxquels la machine virtuelle est connectée.</span><span class="sxs-lookup"><span data-stu-id="66bbc-412">Strings that specify the friendly names of the virtual switches the virtual machine is connected to.</span></span>

<span data-ttu-id="66bbc-413">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="66bbc-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="66bbc-414">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="66bbc-414">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66bbc-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="66bbc-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66bbc-416">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="66bbc-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66bbc-417">Sous-type du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="66bbc-417">The subtype of the virtual system.</span></span>

<span data-ttu-id="66bbc-418">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="66bbc-418">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="66bbc-419">**Microsoft : Hyper-V : sous-type : 1** ()</span><span class="sxs-lookup"><span data-stu-id="66bbc-419">**Microsoft:Hyper-V:SubType:1** ()</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="66bbc-420">**Microsoft : Hyper-V : sous-type : 2** ()</span><span class="sxs-lookup"><span data-stu-id="66bbc-420">**Microsoft:Hyper-V:SubType:2** ()</span></span>


<span data-ttu-id="66bbc-421"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="66bbc-421"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="66bbc-422">Notes</span><span class="sxs-lookup"><span data-stu-id="66bbc-422">Remarks</span></span>

<span data-ttu-id="66bbc-423">L’accès à la classe **MSVM \_ SummaryInformation** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="66bbc-423">Access to the **Msvm\_SummaryInformation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="66bbc-424">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="66bbc-424">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="66bbc-425">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66bbc-425">Requirements</span></span>



| <span data-ttu-id="66bbc-426">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66bbc-426">Requirement</span></span> | <span data-ttu-id="66bbc-427">Valeur</span><span class="sxs-lookup"><span data-stu-id="66bbc-427">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bbc-428">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66bbc-428">Minimum supported client</span></span><br/> | <span data-ttu-id="66bbc-429">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66bbc-429">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="66bbc-430">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66bbc-430">Minimum supported server</span></span><br/> | <span data-ttu-id="66bbc-431">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66bbc-431">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66bbc-432">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66bbc-432">Namespace</span></span><br/>                | <span data-ttu-id="66bbc-433">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="66bbc-433">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="66bbc-434">MOF</span><span class="sxs-lookup"><span data-stu-id="66bbc-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66bbc-435"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66bbc-435"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66bbc-436">DLL</span><span class="sxs-lookup"><span data-stu-id="66bbc-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66bbc-437"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66bbc-437"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66bbc-438">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66bbc-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66bbc-439">**MSVM \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="66bbc-439">**Msvm\_SummaryInformationBase**</span></span>](msvm-summaryinformationbase.md)
</dt> <dt>

[<span data-ttu-id="66bbc-440">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="66bbc-440">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

