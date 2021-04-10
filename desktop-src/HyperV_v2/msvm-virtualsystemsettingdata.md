---
description: Représente les paramètres spécifiques à la virtualisation pour un ordinateur virtuel.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Classe Msvm_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950989"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="93d43-103">MSVM \_ VirtualSystemSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="93d43-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="93d43-104">Représente les paramètres spécifiques à la virtualisation pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="93d43-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="93d43-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d43-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93d43-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="93d43-107">Membres</span><span class="sxs-lookup"><span data-stu-id="93d43-107">Members</span></span>

<span data-ttu-id="93d43-108">La classe **MSVM \_ VirtualSystemSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="93d43-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="93d43-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93d43-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93d43-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="93d43-110">Properties</span></span>

<span data-ttu-id="93d43-111">La classe **MSVM \_ VirtualSystemSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93d43-112">**AdditionalRecoveryInformation**</span><span class="sxs-lookup"><span data-stu-id="93d43-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-114">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-115">Toutes les informations supplémentaires fournies à l’action de récupération.</span><span class="sxs-lookup"><span data-stu-id="93d43-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="93d43-116">La signification de cette propriété est définie par l’action dans **AutomaticRecoveryAction**.</span><span class="sxs-lookup"><span data-stu-id="93d43-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="93d43-117">Si **AutomaticRecoveryAction** a la valeur 0 (« None ») ou 1 (« Restart »), cette valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="93d43-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="93d43-118">Si **AutomaticRecoveryAction** a la valeur 2 (« revenir à l’instantané »), il s’agit du chemin d’accès de l’objet à un instantané qui doit être appliqué en cas d’échec du processus de travail de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-119">**AllowFullSCSICommandSet**</span><span class="sxs-lookup"><span data-stu-id="93d43-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-122">**True** si les commandes SCSI du système d’exploitation invité sont transmises aux disques directs ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="93d43-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="93d43-123">Si la **valeur est true**, les commandes SCSI émises par le système d’exploitation invité sur des disques directs ne sont pas filtrées.</span><span class="sxs-lookup"><span data-stu-id="93d43-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="93d43-124">Nous recommandons que le filtrage SCSI reste activé pour les déploiements de production.</span><span class="sxs-lookup"><span data-stu-id="93d43-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-125">**AllowReducedFcRedundancy**</span><span class="sxs-lookup"><span data-stu-id="93d43-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-128">Spécifie si la migration dynamique d’un ordinateur virtuel qui est configuré avec une carte Fibre Channel virtuelle est autorisée sur un ordinateur de destination qui peut avoir des chemins d’accès non ou réduits aux appareils Fibre Channel cibles.</span><span class="sxs-lookup"><span data-stu-id="93d43-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="93d43-129">Cette propriété doit être désactivée après une migration dynamique.</span><span class="sxs-lookup"><span data-stu-id="93d43-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="93d43-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-130">Value</span></span>                                                                            | <span data-ttu-id="93d43-131">Signification</span><span class="sxs-lookup"><span data-stu-id="93d43-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93d43-132"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="93d43-133">L’ordinateur virtuel ne peut pas être migré dynamiquement vers un ordinateur cible qui peut ne pas avoir de chemins d’accès à la cible de Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="93d43-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="93d43-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="93d43-135">La machine virtuelle peut être migrée dynamiquement vers un ordinateur cible qui peut ne pas avoir de chemins d’accès réduits aux appareils Fibre Channel cibles.</span><span class="sxs-lookup"><span data-stu-id="93d43-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="93d43-136">Le système d’exploitation invité peut perdre la connectivité au stockage et peut se comporter de façon imprévisible.</span><span class="sxs-lookup"><span data-stu-id="93d43-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="93d43-137">**Architecture**</span><span class="sxs-lookup"><span data-stu-id="93d43-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-140">Architecture de ce système.</span><span class="sxs-lookup"><span data-stu-id="93d43-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-141">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93d43-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="93d43-142">**x64** ()</span><span class="sxs-lookup"><span data-stu-id="93d43-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="93d43-143">**arm64** ()</span><span class="sxs-lookup"><span data-stu-id="93d43-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-144">**AutomaticCriticalErrorAction**</span><span class="sxs-lookup"><span data-stu-id="93d43-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-145">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-146">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-147">Identifie l’action à entreprendre sur la machine virtuelle, lorsqu’une erreur critique se produit, comme la déconnexion du stockage.</span><span class="sxs-lookup"><span data-stu-id="93d43-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-148">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="93d43-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="93d43-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-150">Aucune action spécifique n’est effectuée pour les conditions d’erreur critique.</span><span class="sxs-lookup"><span data-stu-id="93d43-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="93d43-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Suspendre la reprise** (1)</span><span class="sxs-lookup"><span data-stu-id="93d43-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-152">Entraîne la suspension de la machine virtuelle et sa reprise automatique lorsque la condition d’erreur critique est résolue.</span><span class="sxs-lookup"><span data-stu-id="93d43-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-153">**AutomaticCriticalErrorActionTimeout**</span><span class="sxs-lookup"><span data-stu-id="93d43-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-154">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93d43-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93d43-156">Qualificateurs : [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« Interval »)</span><span class="sxs-lookup"><span data-stu-id="93d43-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="93d43-157">Identifie la durée maximale d’exécution du **AutomaticCriticalErrorAction** pour résoudre l’erreur critique.</span><span class="sxs-lookup"><span data-stu-id="93d43-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="93d43-158">Cela s’applique uniquement lorsque la valeur de la propriété **AutomaticCriticalErrorAction** n’est pas 0 (aucun).</span><span class="sxs-lookup"><span data-stu-id="93d43-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="93d43-159">Une fois le délai d’attente expiré, la machine virtuelle est mise hors tension.</span><span class="sxs-lookup"><span data-stu-id="93d43-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="93d43-160">La valeur est arrondie à la minute la plus proche.</span><span class="sxs-lookup"><span data-stu-id="93d43-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="93d43-161">La valeur 0 indique que la machine virtuelle doit être mise hors tension immédiatement lorsqu’elle rencontre une condition d’erreur critique.</span><span class="sxs-lookup"><span data-stu-id="93d43-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-162">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-163">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="93d43-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-164">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-166">Action à entreprendre pour l’ordinateur virtuel lors de l’échec du logiciel exécuté par l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="93d43-167">Dans ce cas, les échecs signifient qu’il s’agit d’une défaillance pouvant être détectée par la plateforme hôte, par exemple une condition d’état d’attente non interruptibles.</span><span class="sxs-lookup"><span data-stu-id="93d43-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="93d43-168">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="93d43-169">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-169">This can be one of the following values.</span></span>



| <span data-ttu-id="93d43-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-170">Value</span></span>                                                                               | <span data-ttu-id="93d43-171">Signification</span><span class="sxs-lookup"><span data-stu-id="93d43-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="93d43-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="93d43-173">Aucun</span><span class="sxs-lookup"><span data-stu-id="93d43-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="93d43-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="93d43-175">Redémarrer.</span><span class="sxs-lookup"><span data-stu-id="93d43-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="93d43-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="93d43-177">Revenir à l’instantané.</span><span class="sxs-lookup"><span data-stu-id="93d43-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="93d43-178"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="93d43-179">Réservé.</span><span class="sxs-lookup"><span data-stu-id="93d43-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="93d43-180">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="93d43-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-181">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-183">Action à entreprendre pour l’ordinateur virtuel lorsque l’ordinateur hôte est arrêté.</span><span class="sxs-lookup"><span data-stu-id="93d43-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="93d43-184">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="93d43-185">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-185">This can be one of the following values.</span></span>



| <span data-ttu-id="93d43-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-186">Value</span></span>                                                                               | <span data-ttu-id="93d43-187">Signification</span><span class="sxs-lookup"><span data-stu-id="93d43-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="93d43-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="93d43-189">Désactiver.</span><span class="sxs-lookup"><span data-stu-id="93d43-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="93d43-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="93d43-191">Enregistrer l’État.</span><span class="sxs-lookup"><span data-stu-id="93d43-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="93d43-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="93d43-193">Arrêter.</span><span class="sxs-lookup"><span data-stu-id="93d43-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="93d43-194"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="93d43-195">Réservé.</span><span class="sxs-lookup"><span data-stu-id="93d43-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="93d43-196">**AutomaticSnapshotsEnabled**</span><span class="sxs-lookup"><span data-stu-id="93d43-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-197">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-198">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-199">Indique si les instantanés automatiques doivent être activés sur cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-200">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93d43-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-201">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="93d43-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-202">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-204">Action à effectuer pour l’ordinateur virtuel au démarrage de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="93d43-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="93d43-205">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="93d43-206">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-206">This can be one of the following values.</span></span>



| <span data-ttu-id="93d43-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-207">Value</span></span>                                                                               | <span data-ttu-id="93d43-208">Signification</span><span class="sxs-lookup"><span data-stu-id="93d43-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="93d43-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="93d43-210">Aucun</span><span class="sxs-lookup"><span data-stu-id="93d43-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="93d43-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="93d43-212">Redémarrer si l’activité était déjà active.</span><span class="sxs-lookup"><span data-stu-id="93d43-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="93d43-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="93d43-214">Toujours démarrer.</span><span class="sxs-lookup"><span data-stu-id="93d43-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="93d43-215"><dt>5.. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="93d43-216">Réservé.</span><span class="sxs-lookup"><span data-stu-id="93d43-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="93d43-217">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="93d43-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-218">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93d43-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-219">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-220">Délai avant le démarrage automatique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="93d43-221">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-222">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="93d43-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-223">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-225">Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte.</span><span class="sxs-lookup"><span data-stu-id="93d43-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="93d43-226">Un nombre inférieur indique une activation antérieure.</span><span class="sxs-lookup"><span data-stu-id="93d43-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="93d43-227">Si une ou plusieurs configurations affichent la même valeur, la séquence dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="93d43-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="93d43-228">La valeur 0 indique que la séquence dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="93d43-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="93d43-229">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-230">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="93d43-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-233">Numéro de série du tableau de base pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="93d43-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-234">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="93d43-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-235">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-236">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-237">Identificateur global unique du BIOS de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-238">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="93d43-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-239">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-240">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-241">**True** si la touche VERR. num est activée (on) par le BIOS ; **False** si la touche VERR. num est désactivée (OFF) par le BIOS.</span><span class="sxs-lookup"><span data-stu-id="93d43-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="93d43-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-245">Numéro de série du BIOS de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-246">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="93d43-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-247">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93d43-248">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93d43-249">Qualificateurs : [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="93d43-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="93d43-250">L’ordre de démarrage défini dans le BIOS de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="93d43-251">Cette propriété est un tableau de valeurs, comprise entre **BootOrder** \[ 0 \] et **BootOrder** \[ 3 \] , inclus, où chaque valeur indique un appareil à partir duquel démarrer.</span><span class="sxs-lookup"><span data-stu-id="93d43-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="93d43-252">Chacune des 4 valeurs du tableau doit être définie et ne doit pas être la même qu’une autre valeur dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="93d43-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="93d43-253">L’ordinateur virtuel tente d’abord de démarrer à partir de l’appareil indiqué par la première valeur dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="93d43-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="93d43-254">Si cet appareil ne contient pas de secteur de démarrage, l’ordinateur virtuel tente de démarrer à partir du périphérique suivant spécifié par la propriété **BootOrder** , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="93d43-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="93d43-255">Si aucun périphérique spécifié dans le **BootOrder** ne contient de secteur de démarrage, l’ordinateur virtuel ne pourra pas démarrer.</span><span class="sxs-lookup"><span data-stu-id="93d43-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="93d43-256">La valeur par défaut d’un ordinateur virtuel est \[ 0, 1, 2, 3 \] .</span><span class="sxs-lookup"><span data-stu-id="93d43-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="93d43-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Disquette** (0)</span><span class="sxs-lookup"><span data-stu-id="93d43-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-258">L’ordinateur virtuel tente de démarrer à partir de la disquette dans le lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="93d43-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="93d43-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span><span class="sxs-lookup"><span data-stu-id="93d43-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-260">L’ordinateur virtuel tente de démarrer à partir du premier disque CD ou DVD trouvé avec un secteur d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="93d43-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="93d43-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Disque dur IDE** (2)</span><span class="sxs-lookup"><span data-stu-id="93d43-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-262">L’ordinateur virtuel tente de démarrer à partir du premier lecteur de disque dur trouvé avec un secteur d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="93d43-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="93d43-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Démarrage PXE** (3)</span><span class="sxs-lookup"><span data-stu-id="93d43-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-264">L’ordinateur virtuel tentera un démarrage PXE à partir du réseau.</span><span class="sxs-lookup"><span data-stu-id="93d43-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="93d43-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Disque dur SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="93d43-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="93d43-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Réservé** (5.. 65535)</span><span class="sxs-lookup"><span data-stu-id="93d43-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-267">**BootSourceOrder**</span><span class="sxs-lookup"><span data-stu-id="93d43-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-268">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="93d43-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93d43-269">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-270">Ordre de la source de démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="93d43-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="93d43-271">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93d43-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-272">**Caption**</span><span class="sxs-lookup"><span data-stu-id="93d43-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-275">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="93d43-275">A short description of the object.</span></span> <span data-ttu-id="93d43-276">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93d43-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-277">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="93d43-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-278">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-279">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-280">Numéro d’inventaire du châssis de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="93d43-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-281">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="93d43-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-283">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-284">Numéro de série du châssis de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-285">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="93d43-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-288">Chemin d’accès d’un répertoire où sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="93d43-289">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-290">**Fichier ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="93d43-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-291">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-293">Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="93d43-294">Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="93d43-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="93d43-295">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="93d43-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-299">Identificateur unique de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="93d43-300">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-301">**ConsoleMode**</span><span class="sxs-lookup"><span data-stu-id="93d43-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-302">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-303">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-304">Identifie le mode de console de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="93d43-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-305">Cette propriété a été ajoutée dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="93d43-306">**Valeur par défaut** (0)</span><span class="sxs-lookup"><span data-stu-id="93d43-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="93d43-307">**COM1** (1)</span><span class="sxs-lookup"><span data-stu-id="93d43-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="93d43-308">**COM2** (2)</span><span class="sxs-lookup"><span data-stu-id="93d43-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="93d43-309">**Aucun** (3)</span><span class="sxs-lookup"><span data-stu-id="93d43-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="93d43-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-311">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93d43-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-313">Date et heure de création des paramètres de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="93d43-314">Si cet objet représente les paramètres actuels de l’ordinateur virtuel, cette valeur correspond à l’heure à laquelle le système a été créé.</span><span class="sxs-lookup"><span data-stu-id="93d43-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="93d43-315">Si cet objet représente les paramètres d’instantané de la machine virtuelle, cette valeur correspond à l’heure à laquelle l’instantané a été pris.</span><span class="sxs-lookup"><span data-stu-id="93d43-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="93d43-316">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-317">**DebugChannelId**</span><span class="sxs-lookup"><span data-stu-id="93d43-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-318">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93d43-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-319">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-320">Identificateur de canal utilisé pour déboguer l’ordinateur virtuel à l’aide du débogueur unifié.</span><span class="sxs-lookup"><span data-stu-id="93d43-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-321">**DebugPort**</span><span class="sxs-lookup"><span data-stu-id="93d43-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-322">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93d43-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-323">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-324">Port TCP/IP utilisé pour déboguer l’ordinateur virtuel à l’aide du débogage synthétique.</span><span class="sxs-lookup"><span data-stu-id="93d43-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-325">**DebugPortEnabled**</span><span class="sxs-lookup"><span data-stu-id="93d43-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-326">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-327">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-328">Spécifie si l’ordinateur virtuel utilise le débogage synthétique.</span><span class="sxs-lookup"><span data-stu-id="93d43-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="93d43-329">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="93d43-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="93d43-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="93d43-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**Activé** (1)</span><span class="sxs-lookup"><span data-stu-id="93d43-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="93d43-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span><span class="sxs-lookup"><span data-stu-id="93d43-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-333">Affecté automatiquement</span><span class="sxs-lookup"><span data-stu-id="93d43-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-334">**Description**</span><span class="sxs-lookup"><span data-stu-id="93d43-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-337">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="93d43-337">A description of the object.</span></span> <span data-ttu-id="93d43-338">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="93d43-339">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-339">Value</span></span>                                                                                                                  | <span data-ttu-id="93d43-340">Signification</span><span class="sxs-lookup"><span data-stu-id="93d43-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="93d43-341"><dt>« Paramètres actifs pour la machine virtuelle »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="93d43-342">Cette instance fait référence à un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="93d43-343"><dt>« Paramètres d’instantané de la machine virtuelle »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="93d43-344">Cette instance fait référence à un instantané.</span><span class="sxs-lookup"><span data-stu-id="93d43-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="93d43-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93d43-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-347">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-348">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="93d43-348">A display name for the object.</span></span> <span data-ttu-id="93d43-349">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))et est toujours définie sur le nom complet de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="93d43-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="93d43-350">Ce nom ne doit pas dépasser 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="93d43-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-351">**EnhancedSessionTransportType**</span><span class="sxs-lookup"><span data-stu-id="93d43-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-352">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-353">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-354">Indique le type de transport à utiliser lors de la connexion à une session étendue.</span><span class="sxs-lookup"><span data-stu-id="93d43-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-355">Cette propriété a été ajoutée dans Windows 10, version 1803.</span><span class="sxs-lookup"><span data-stu-id="93d43-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="93d43-356">**Canal VMBus** (0)</span><span class="sxs-lookup"><span data-stu-id="93d43-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="93d43-357">**Socket Hyper-V** (1)</span><span class="sxs-lookup"><span data-stu-id="93d43-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-358">**GuestControlledCacheTypes**</span><span class="sxs-lookup"><span data-stu-id="93d43-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-359">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-360">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-361">Indique si l’invité peut contrôler les types de cache.</span><span class="sxs-lookup"><span data-stu-id="93d43-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-362">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-363">**GuestStateDataRoot**</span><span class="sxs-lookup"><span data-stu-id="93d43-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-365">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-366">Chemin d’un répertoire où sont stockées les informations relatives à l’état d’exécution invité.</span><span class="sxs-lookup"><span data-stu-id="93d43-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-367">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93d43-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-368">**GuestStateFile**</span><span class="sxs-lookup"><span data-stu-id="93d43-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-369">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-370">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-371">Chemin d’accès d’un fichier dans lequel les informations relatives à l’état d’exécution invité sont stockées.</span><span class="sxs-lookup"><span data-stu-id="93d43-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="93d43-372">Un chemin d’accès relatif ajoute à la valeur de la propriété **GuestStateDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="93d43-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-373">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93d43-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-374">**HighMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="93d43-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-375">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93d43-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-376">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-377">La taille du haut (au-dessus de 4 Go) Memory-Mapped écart d’e/s en Mo</span><span class="sxs-lookup"><span data-stu-id="93d43-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="93d43-378">Cette propriété a été ajoutée dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="93d43-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-379">**IncrementalBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="93d43-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-380">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-381">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-382">Indique si l’enregistreur VSS Hyper-V prend en charge les sauvegardes incrémentielles de cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93d43-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-384">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-385">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93d43-386">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="93d43-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93d43-387">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="93d43-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93d43-388">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-389">**IsAutomaticSnapshot**</span><span class="sxs-lookup"><span data-stu-id="93d43-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-390">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-392">Indique s’il s’agit d’un instantané créé automatiquement pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93d43-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-393">Ajouté dans Windows 10, version 1709.</span><span class="sxs-lookup"><span data-stu-id="93d43-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="93d43-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-395">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-396">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-397">**True** si la configuration a une référence à un fichier d’état enregistré ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="93d43-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="93d43-398">Cela n’indique pas la présence d’un tel fichier, mais uniquement que la configuration en spécifie une.</span><span class="sxs-lookup"><span data-stu-id="93d43-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-399">**LockOnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="93d43-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-400">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-401">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-402">Verrouiller la console lors de la déconnexion de vmconnect.</span><span class="sxs-lookup"><span data-stu-id="93d43-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-403">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-404">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="93d43-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-405">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-406">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-407">Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="93d43-408">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-409">**LowMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="93d43-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-410">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93d43-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-411">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-412">Configure la taille, en mégaoctets, du premier intervalle MMIO pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="93d43-413">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93d43-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="93d43-414">Plage : 128 3584</span><span class="sxs-lookup"><span data-stu-id="93d43-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="93d43-415">**NetworkBootPreferredProtocol**</span><span class="sxs-lookup"><span data-stu-id="93d43-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-416">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-417">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-418">Détermine si le protocole préféré pour le démarrage PXE est IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="93d43-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="93d43-419">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93d43-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="93d43-420">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="93d43-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="93d43-421">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="93d43-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-422">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="93d43-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-423">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="93d43-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93d43-424">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-425">Les notes fournies par l’utilisateur sont liées à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="93d43-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="93d43-426">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-427">**Parent**</span><span class="sxs-lookup"><span data-stu-id="93d43-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-428">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-429">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-430">Si cette instance ne représente pas un système basé sur un instantané d’un ordinateur virtuel, cette propriété a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="93d43-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="93d43-431">Sinon, la propriété contient le chemin d’accès de l’objet **MSVM \_ VirtualSystemSettingData** sur lequel cette instance est basée.</span><span class="sxs-lookup"><span data-stu-id="93d43-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="93d43-432">Lors de la création d’une hiérarchie d’arborescence d’instantanés pour l’ordinateur virtuel, cette propriété fait référence à l’objet à partir duquel l’instance actuelle est dérivée (l’instance actuelle est le nœud enfant et l’objet référencé dans cette propriété est le nœud parent).</span><span class="sxs-lookup"><span data-stu-id="93d43-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="93d43-433">**ParentPackage**</span><span class="sxs-lookup"><span data-stu-id="93d43-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-434">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-435">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-436">Si ce système est un conteneur, le chemin d’accès au \_ ContainerPackage MSVM à partir duquel ce système est basé.</span><span class="sxs-lookup"><span data-stu-id="93d43-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-437">Ajouté dans Windows 10 ; supprimé dans Windows 10, version 1703.</span><span class="sxs-lookup"><span data-stu-id="93d43-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-438">**PauseAfterBootFailure**</span><span class="sxs-lookup"><span data-stu-id="93d43-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-439">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-440">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-441">Indique si le BIOS s’interrompt après chaque échec d’entrée de démarrage en attendant que l’utilisateur appuie sur une touche.</span><span class="sxs-lookup"><span data-stu-id="93d43-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="93d43-442">**True** si le BIOS s’arrête ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="93d43-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="93d43-443">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93d43-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-444">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="93d43-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-447">Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="93d43-448">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-449">**SecureBootEnabled**</span><span class="sxs-lookup"><span data-stu-id="93d43-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-450">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-451">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-452">Indique si le démarrage sécurisé est activé pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="93d43-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="93d43-453">**True** si l’option est activée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="93d43-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-454">Le démarrage sécurisé ne peut être activé que pour les machines virtuelles de génération 2.</span><span class="sxs-lookup"><span data-stu-id="93d43-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="93d43-455">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93d43-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-456">**SecureBootTemplateId**</span><span class="sxs-lookup"><span data-stu-id="93d43-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-458">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-459">Identificateur global unique du modèle de valeurs initiales des variables liées au démarrage sécurisé UEFI.</span><span class="sxs-lookup"><span data-stu-id="93d43-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="93d43-460">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="93d43-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-461">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="93d43-462">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="93d43-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-464">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-465">Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="93d43-466">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-467">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="93d43-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-468">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-469">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-470">Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="93d43-471">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-472">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="93d43-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-473">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-474">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-475">Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="93d43-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="93d43-476">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-477">**UserSnapshotType**</span><span class="sxs-lookup"><span data-stu-id="93d43-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-478">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93d43-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-479">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="93d43-480">Indique le type d’instantané défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="93d43-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="93d43-481">Ajouté dans Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="93d43-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="93d43-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (2)</span><span class="sxs-lookup"><span data-stu-id="93d43-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-483">Désactivez la création d’un instantané.</span><span class="sxs-lookup"><span data-stu-id="93d43-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="93d43-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span><span class="sxs-lookup"><span data-stu-id="93d43-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-485">Instantané de cohérence des données à utiliser dans l’environnement de production. Effectue un instantané avec l’état de l’application lorsque la possibilité de créer un instantané de cohérence des données n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="93d43-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="93d43-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span><span class="sxs-lookup"><span data-stu-id="93d43-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-487">Instantané de cohérence des données à utiliser dans l’environnement de production. Ne crée pas d’instantané avec l’état de l’application s’il n’est pas possible de créer un instantané de cohérence des données.</span><span class="sxs-lookup"><span data-stu-id="93d43-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="93d43-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span><span class="sxs-lookup"><span data-stu-id="93d43-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="93d43-489">Instantané qui contient des informations sur la mémoire et l’appareil à des fins de test et de développement.</span><span class="sxs-lookup"><span data-stu-id="93d43-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-490">**Version**</span><span class="sxs-lookup"><span data-stu-id="93d43-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-491">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-492">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-493">Version de la machine virtuelle dans un format « major. minor », par exemple « 2,0 ».</span><span class="sxs-lookup"><span data-stu-id="93d43-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="93d43-494">**VirtualNumaEnabled**</span><span class="sxs-lookup"><span data-stu-id="93d43-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-495">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="93d43-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-496">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="93d43-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="93d43-497">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**","[**MSVM \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span><span class="sxs-lookup"><span data-stu-id="93d43-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="93d43-498">**True** si des nœuds NUMA (non-Uniform Memory Access) virtuels sont projetés dans l’ordinateur virtuel ; **False** si l’ordinateur virtuel a un seul nœud.</span><span class="sxs-lookup"><span data-stu-id="93d43-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="93d43-499">Si la **valeur est true**, le nombre de nœuds NUMA virtuels projetés dans l’ordinateur virtuel est déterminé à partir des valeurs des propriétés [**MSVM \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) et [**MSVM MemorySettingData. \_ MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="93d43-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="93d43-500">**Attribut virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="93d43-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-501">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-502">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93d43-503">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData. attribut virtualsystemidentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM CIM \_**](cim-computersystem.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="93d43-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="93d43-504">Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="93d43-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="93d43-505">Cette propriété est une substitution de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93d43-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93d43-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="93d43-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-507">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-508">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-509">Les valeurs valides pour cette propriété sont Microsoft : Hyper-V : SubType : 1 et Microsoft : Hyper-V : SubType : 2.</span><span class="sxs-lookup"><span data-stu-id="93d43-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="93d43-510">Une machine virtuelle de génération 1 est SubType 1.</span><span class="sxs-lookup"><span data-stu-id="93d43-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="93d43-511">Une machine virtuelle de génération 2 est sous-type 2.</span><span class="sxs-lookup"><span data-stu-id="93d43-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="93d43-512">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="93d43-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="93d43-513">**Microsoft : Hyper-v : sous-type : 1** (« Microsoft : Hyper-v : SubType : 1 »)</span><span class="sxs-lookup"><span data-stu-id="93d43-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="93d43-514">**Microsoft : Hyper-v : sous-type : 2** (« Microsoft : Hyper-v : SubType : 2 »)</span><span class="sxs-lookup"><span data-stu-id="93d43-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="93d43-515">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="93d43-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d43-516">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="93d43-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93d43-517">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="93d43-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93d43-518">Spécifie le type de machine virtuelle que les données de paramètre représentent.</span><span class="sxs-lookup"><span data-stu-id="93d43-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="93d43-519">Cette propriété est héritée de la classe [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="93d43-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="93d43-520">Il s’agit de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="93d43-520">This will be one of the following values.</span></span>



| <span data-ttu-id="93d43-521">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="93d43-522">Signification</span><span class="sxs-lookup"><span data-stu-id="93d43-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="93d43-523"><dt>« Microsoft : Hyper-V : système : réalisé »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="93d43-524">Un ordinateur virtuel réalisé.</span><span class="sxs-lookup"><span data-stu-id="93d43-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="93d43-525"><dt>« Microsoft : Hyper-V : système : planifié »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="93d43-526">Un ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="93d43-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="93d43-527"><dt>« Microsoft : Hyper-V : instantané : réalisé »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="93d43-528">Instantané d’un ordinateur virtuel réalisé.</span><span class="sxs-lookup"><span data-stu-id="93d43-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="93d43-529"><dt>« Microsoft : Hyper-V : capture instantanée : récupération »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="93d43-530">Instantané d’un ordinateur virtuel de récupération.</span><span class="sxs-lookup"><span data-stu-id="93d43-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="93d43-531"><dt>« Microsoft : Hyper-V : instantané : planifié »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="93d43-532">Instantané d’un ordinateur virtuel planifié.</span><span class="sxs-lookup"><span data-stu-id="93d43-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="93d43-533"><dt>« Microsoft : Hyper-V : instantané : manquant »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="93d43-534">Instantané manquant.</span><span class="sxs-lookup"><span data-stu-id="93d43-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="93d43-535"><dt>« Microsoft : Hyper-V : instantané : réplica : standard »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="93d43-536">Instantané de point de réplication basé sur l’heure.</span><span class="sxs-lookup"><span data-stu-id="93d43-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="93d43-537"><dt>« Microsoft : Hyper-V : instantané : réplica : ApplicationConsistent »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="93d43-538">Instantané de point de réplication VSS.</span><span class="sxs-lookup"><span data-stu-id="93d43-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="93d43-539"><dt>« Microsoft : Hyper-V : instantané : réplica : PlannedFailover »</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="93d43-540">Instantané de réplication planifiée.</span><span class="sxs-lookup"><span data-stu-id="93d43-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93d43-541">Notes</span><span class="sxs-lookup"><span data-stu-id="93d43-541">Remarks</span></span>

<span data-ttu-id="93d43-542">L’accès à la classe **MSVM \_ VirtualSystemSettingData** peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="93d43-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="93d43-543">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="93d43-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="93d43-544">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93d43-544">Requirements</span></span>



| <span data-ttu-id="93d43-545">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93d43-545">Requirement</span></span> | <span data-ttu-id="93d43-546">Valeur</span><span class="sxs-lookup"><span data-stu-id="93d43-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d43-547">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93d43-547">Minimum supported client</span></span><br/> | <span data-ttu-id="93d43-548">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93d43-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93d43-549">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="93d43-549">Minimum supported server</span></span><br/> | <span data-ttu-id="93d43-550">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="93d43-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93d43-551">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="93d43-551">Namespace</span></span><br/>                | <span data-ttu-id="93d43-552">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="93d43-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93d43-553">MOF</span><span class="sxs-lookup"><span data-stu-id="93d43-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93d43-554"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93d43-555">DLL</span><span class="sxs-lookup"><span data-stu-id="93d43-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93d43-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93d43-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93d43-557">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93d43-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d43-558">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="93d43-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="93d43-559">[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93d43-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="93d43-560">Classes du système virtuel</span><span class="sxs-lookup"><span data-stu-id="93d43-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

