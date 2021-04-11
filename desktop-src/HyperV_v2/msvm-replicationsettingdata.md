---
description: Représente les paramètres spécifiques à la réplication pour un ordinateur virtuel.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Classe Msvm_ReplicationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203414"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="7fc19-103">MSVM \_ ReplicationSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="7fc19-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="7fc19-104">Représente les paramètres spécifiques à la réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="7fc19-105">Le client passe une instance de cette classe à [**MSVM \_ ReplicationService. CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) pour créer une relation de réplication.</span><span class="sxs-lookup"><span data-stu-id="7fc19-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="7fc19-106">Le client ne peut pas modifier directement les valeurs des propriétés de cette classe ; il doit appeler la méthode [**MSVM \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) pour modifier les valeurs.</span><span class="sxs-lookup"><span data-stu-id="7fc19-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="7fc19-107">Chaque relation de réplication possède une seule instance de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7fc19-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="7fc19-108">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7fc19-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc19-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fc19-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="7fc19-110">Membres</span><span class="sxs-lookup"><span data-stu-id="7fc19-110">Members</span></span>

<span data-ttu-id="7fc19-111">La classe **MSVM \_ ReplicationSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7fc19-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7fc19-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fc19-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fc19-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7fc19-113">Properties</span></span>

<span data-ttu-id="7fc19-114">La classe **MSVM \_ ReplicationSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7fc19-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fc19-115">**AdditionalSettings**</span><span class="sxs-lookup"><span data-stu-id="7fc19-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-118">Paramètres de réplication supplémentaires que le fournisseur de point de terminaison peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="7fc19-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="7fc19-119">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7fc19-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-120">**ApplicationConsistentSnapshotInterval**</span><span class="sxs-lookup"><span data-stu-id="7fc19-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-121">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-123">Intervalle de temps entre les captures instantanées cohérentes de l’application, spécifié en heures.</span><span class="sxs-lookup"><span data-stu-id="7fc19-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="7fc19-124">Les valeurs valides sont comprises entre 1 heure et 12 heures.</span><span class="sxs-lookup"><span data-stu-id="7fc19-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="7fc19-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-126">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-128">Définit le mode d’authentification utilisé pour se connecter au serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="7fc19-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="7fc19-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Authentification Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="7fc19-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7fc19-130">Authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="7fc19-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="7fc19-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Authentification basée sur les certificats** (2)</span><span class="sxs-lookup"><span data-stu-id="7fc19-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7fc19-132">Authentification basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="7fc19-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7fc19-133">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="7fc19-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-134">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-136">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7fc19-136">Not used.</span></span>

<span data-ttu-id="7fc19-137">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-138">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="7fc19-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-139">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-141">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7fc19-141">Not used.</span></span>

<span data-ttu-id="7fc19-142">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-143">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="7fc19-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-144">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-146">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7fc19-146">Not used.</span></span>

<span data-ttu-id="7fc19-147">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-148">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="7fc19-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-149">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fc19-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-151">Délai avant le démarrage automatique de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="7fc19-152">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-153">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="7fc19-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-156">Nombre qui indique la séquence relative d’activation d’ordinateur virtuel lors du démarrage du système hôte.</span><span class="sxs-lookup"><span data-stu-id="7fc19-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="7fc19-157">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-158">**AutoResynchronizeEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fc19-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-159">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fc19-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-161">Spécifie si les opérations de resynchronisation sont déclenchées automatiquement lorsqu’une erreur de réplication se produit en raison de défaillances de l’alimentation et du matériel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="7fc19-162">Les opérations de resynchronisation ne sont déclenchées que lorsque l’échec se produit entre les heures spécifiées par les propriétés **AutoResynchronizeIntervalStart** et **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="7fc19-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="7fc19-163">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="7fc19-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-164">**AutoResynchronizeIntervalEnd**</span><span class="sxs-lookup"><span data-stu-id="7fc19-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-165">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fc19-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-167">Spécifie l’heure de fin des opérations de resynchronisation automatique à déclencher.</span><span class="sxs-lookup"><span data-stu-id="7fc19-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="7fc19-168">Cette valeur est en heure locale.</span><span class="sxs-lookup"><span data-stu-id="7fc19-168">This value is in local time.</span></span> <span data-ttu-id="7fc19-169">La valeur par défaut est 06:00 (6:00 A.M.).</span><span class="sxs-lookup"><span data-stu-id="7fc19-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="7fc19-170">Les opérations de resynchronisation ne sont déclenchées que lorsque l’échec se produit entre les heures spécifiées par les propriétés **AutoResynchronizeIntervalStart** et **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="7fc19-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="7fc19-171">Les opérations de resynchronisation peuvent également être planifiées pour être déclenchées au cours de l’intervalle suivant.</span><span class="sxs-lookup"><span data-stu-id="7fc19-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-172">**AutoResynchronizeIntervalStart**</span><span class="sxs-lookup"><span data-stu-id="7fc19-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-173">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fc19-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-175">Spécifie l’heure de début des opérations de resynchronisation automatique à déclencher.</span><span class="sxs-lookup"><span data-stu-id="7fc19-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="7fc19-176">Cette valeur est en heure locale.</span><span class="sxs-lookup"><span data-stu-id="7fc19-176">This value is in local time.</span></span> <span data-ttu-id="7fc19-177">La valeur par défaut est 18:30 (6:30 P.M.).</span><span class="sxs-lookup"><span data-stu-id="7fc19-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="7fc19-178">Les opérations de resynchronisation ne sont déclenchées que lorsque l’échec se produit entre les heures spécifiées par les propriétés **AutoResynchronizeIntervalStart** et **AutoResynchronizeIntervalEnd** .</span><span class="sxs-lookup"><span data-stu-id="7fc19-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="7fc19-179">Les opérations de resynchronisation peuvent également être planifiées pour être déclenchées au cours de l’intervalle suivant.</span><span class="sxs-lookup"><span data-stu-id="7fc19-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-180">**BypassProxyServer**</span><span class="sxs-lookup"><span data-stu-id="7fc19-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-181">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fc19-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-183">Spécifie si le serveur proxy doit être contourné lors de la connexion à un serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="7fc19-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7fc19-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-186">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-187">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7fc19-187">A short description of the object.</span></span> <span data-ttu-id="7fc19-188">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres de réplication ».</span><span class="sxs-lookup"><span data-stu-id="7fc19-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-189">**Empreinte**</span><span class="sxs-lookup"><span data-stu-id="7fc19-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-192">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="7fc19-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-193">Empreinte numérique du certificat à utiliser lorsque la propriété **AuthenticationType** est l’authentification basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="7fc19-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-194">**CompressionEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fc19-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-195">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fc19-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-197">Spécifie si les données de réplication sont compressées lors de leur envoi au serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="7fc19-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-198">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="7fc19-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-201">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7fc19-201">Not used.</span></span>

<span data-ttu-id="7fc19-202">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-203">**Fichier ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="7fc19-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-206">Chemin d’accès relatif et nom de fichier d’un fichier dans lequel sont stockées les informations relatives à la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="7fc19-207">Ce chemin d’accès est relatif à la propriété **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="7fc19-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="7fc19-208">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="7fc19-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-212">Identificateur unique de la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="7fc19-213">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="7fc19-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-215">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7fc19-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-216">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-217">Date et heure de création des paramètres de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="7fc19-218">Si cet objet représente les paramètres actuels de l’ordinateur virtuel, cette valeur correspond à l’heure à laquelle le système a été créé.</span><span class="sxs-lookup"><span data-stu-id="7fc19-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="7fc19-219">Si cet objet représente les paramètres d’instantané de la machine virtuelle, cette valeur correspond à l’heure à laquelle l’instantané a été pris.</span><span class="sxs-lookup"><span data-stu-id="7fc19-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="7fc19-220">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="7fc19-221">Il s’agit d’une propriété en lecture seule, mais elle peut être modifiée à l’aide de la méthode [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc19-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="7fc19-222">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-223">**Description**</span><span class="sxs-lookup"><span data-stu-id="7fc19-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-226">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="7fc19-226">A description of the object.</span></span> <span data-ttu-id="7fc19-227">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données des paramètres de réplication de l’ordinateur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="7fc19-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7fc19-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-229">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-231">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7fc19-231">A display name for the object.</span></span> <span data-ttu-id="7fc19-232">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))et est définie sur le nom complet de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7fc19-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-233">**EnableWriteOrderPreservationAcrossDisks**</span><span class="sxs-lookup"><span data-stu-id="7fc19-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-234">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fc19-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-236">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (« aucune valeur »)</span><span class="sxs-lookup"><span data-stu-id="7fc19-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-237">Spécifie si tous les disques durs virtuels de réplication de la machine virtuelle sont répliqués au même point dans le temps.</span><span class="sxs-lookup"><span data-stu-id="7fc19-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="7fc19-238">Cela garantit que la réplication honore l’ordre d’écriture des applications dans la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7fc19-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="7fc19-239">**Windows 8.1 :** À partir de Windows 8.1 et de Windows Server 2012 R2, cette propriété est déconseillée et a toujours la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="7fc19-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-240">**IncludedDisks**</span><span class="sxs-lookup"><span data-stu-id="7fc19-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-241">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7fc19-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-243">Qualificateurs : **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexé")</span><span class="sxs-lookup"><span data-stu-id="7fc19-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-244">Liste des disques durs virtuels (VHD) attachés au système qui seront répliqués par le moteur de réplication.</span><span class="sxs-lookup"><span data-stu-id="7fc19-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="7fc19-245">Il s’agit d’un tableau de chaînes, chacune contenant l' **InstanceID** du [**\_ StorageAllocationSettingData MSVM**](msvm-storageallocationsettingdata.md) qui représente le disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7fc19-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-249">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="7fc19-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-250">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="7fc19-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7fc19-251">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="7fc19-252">Pour Windows 8, elle est toujours définie sur « Microsoft :*GUID d’ordinateur virtuel* \\ HVR ».</span><span class="sxs-lookup"><span data-stu-id="7fc19-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="7fc19-253">Par Windows 8.1, elle est définie sur « Microsoft :*GUID d’ordinateur virtuel* \\ HVR \\<0/1> ».</span><span class="sxs-lookup"><span data-stu-id="7fc19-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="7fc19-254">Dans la valeur Windows 8.1, 0 indique primaire et 1 indique la réplication étendue.</span><span class="sxs-lookup"><span data-stu-id="7fc19-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="7fc19-255">Pour plus d’informations sur la réplication étendue, consultez [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="7fc19-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-256">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="7fc19-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-259">Chemin d’accès d’un répertoire dans lequel sont stockées les informations de journalisation de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="7fc19-260">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-261">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="7fc19-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-262">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="7fc19-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-264">Non utilisé et ne peut pas être défini.</span><span class="sxs-lookup"><span data-stu-id="7fc19-264">Not used and can't be set.</span></span>

<span data-ttu-id="7fc19-265">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-266">**PrimaryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="7fc19-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-268">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-269">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7fc19-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-270">Nom du point de connexion principal.</span><span class="sxs-lookup"><span data-stu-id="7fc19-270">The name of the primary connection point.</span></span> <span data-ttu-id="7fc19-271">Dans le cas d’un cluster principal, il s’agit du nom de l’extrémité de service Broker.</span><span class="sxs-lookup"><span data-stu-id="7fc19-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="7fc19-272">Dans le cas d’un serveur principal autonome, il s’agit du nom du système hôte.</span><span class="sxs-lookup"><span data-stu-id="7fc19-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-273">**PrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="7fc19-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-276">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7fc19-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-277">Nom de domaine complet du système hôte principal qui héberge l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-278">**RecoveryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="7fc19-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-281">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7fc19-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-282">Nom du point de connexion de récupération.</span><span class="sxs-lookup"><span data-stu-id="7fc19-282">The name of the recovery connection point.</span></span> <span data-ttu-id="7fc19-283">Dans le cas d’un cluster de récupération, il s’agit du nom de l’extrémité de service Broker.</span><span class="sxs-lookup"><span data-stu-id="7fc19-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="7fc19-284">Dans le cas d’un serveur de récupération autonome, il s’agit du nom du système hôte.</span><span class="sxs-lookup"><span data-stu-id="7fc19-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-285">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="7fc19-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-287">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-288">Chemin d’accès complet d’un fichier dans lequel sont stockées les informations relatives à la récupération de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="7fc19-289">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-290">**RecoveryHistory**</span><span class="sxs-lookup"><span data-stu-id="7fc19-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-291">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-293">Nombre maximal d’instantanés de récupération qui seront stockés sur le serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="7fc19-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="7fc19-294">Les valeurs valides sont comprises entre 0 et 24.</span><span class="sxs-lookup"><span data-stu-id="7fc19-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-295">**RecoveryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="7fc19-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-296">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-298">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7fc19-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-299">Nom de domaine complet du système hôte de récupération qui héberge la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7fc19-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-300">**RecoveryServerPortNumber**</span><span class="sxs-lookup"><span data-stu-id="7fc19-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-301">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-303">Numéro de port du serveur de récupération à utiliser pour établir une connexion sécurisée pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="7fc19-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-304">**ReplicateHostKvpItems**</span><span class="sxs-lookup"><span data-stu-id="7fc19-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-305">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7fc19-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-306">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-307">Spécifie si les [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s de l’ordinateur hôte doivent être répliqués à partir de l’ordinateur virtuel principal vers l’ordinateur virtuel de récupération.</span><span class="sxs-lookup"><span data-stu-id="7fc19-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="7fc19-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-309">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7fc19-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-310">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-311">Intervalle de réplication d’une relation de réplication, en secondes.</span><span class="sxs-lookup"><span data-stu-id="7fc19-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="7fc19-312">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="7fc19-312">Valid values are:</span></span>

<span data-ttu-id="7fc19-313">30</span><span class="sxs-lookup"><span data-stu-id="7fc19-313">30</span></span>

<span data-ttu-id="7fc19-314">300</span><span class="sxs-lookup"><span data-stu-id="7fc19-314">300</span></span>

<span data-ttu-id="7fc19-315">900</span><span class="sxs-lookup"><span data-stu-id="7fc19-315">900</span></span>

<span data-ttu-id="7fc19-316">La valeur par défaut est 300 secondes.</span><span class="sxs-lookup"><span data-stu-id="7fc19-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="7fc19-317">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7fc19-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-318">**ReplicationProvider**</span><span class="sxs-lookup"><span data-stu-id="7fc19-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-321">Chemin d’accès à l’instance de la classe [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) qui identifie le point de terminaison du fournisseur de réplication.</span><span class="sxs-lookup"><span data-stu-id="7fc19-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="7fc19-322">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7fc19-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-323">**RootCertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="7fc19-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-325">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-326">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="7fc19-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-327">Empreinte numérique de certificat racine du certificat en cours d’utilisation lorsque **AuthenticationType** est 2 (autorisation basée sur un certificat).</span><span class="sxs-lookup"><span data-stu-id="7fc19-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-328">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="7fc19-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-329">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-330">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-331">Chemin d’accès d’un répertoire où sont stockées les informations sur les captures instantanées d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="7fc19-332">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-333">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="7fc19-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-335">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-336">Chemin d’accès d’un répertoire où sont stockées les informations relatives aux informations relatives à la suspension de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="7fc19-337">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-338">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="7fc19-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-339">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-340">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-341">Chemin d’accès d’un répertoire où sont stockés les fichiers d’échange de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7fc19-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="7fc19-342">Cette propriété est héritée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), mais elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="7fc19-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-343">**Attribut virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="7fc19-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-344">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-345">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-346">Nom de l’objet [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) auquel appartiennent les données de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7fc19-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="7fc19-347">Cette propriété est une substitution de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7fc19-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7fc19-348">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="7fc19-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fc19-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7fc19-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7fc19-350">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7fc19-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7fc19-351">Spécifie le type de machine virtuelle que les données de paramètre représentent.</span><span class="sxs-lookup"><span data-stu-id="7fc19-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="7fc19-352">Cette propriété est héritée de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))et est toujours définie sur « Microsoft : Hyper-V : réplica ».</span><span class="sxs-lookup"><span data-stu-id="7fc19-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fc19-353">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fc19-353">Requirements</span></span>



| <span data-ttu-id="7fc19-354">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fc19-354">Requirement</span></span> | <span data-ttu-id="7fc19-355">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fc19-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc19-356">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fc19-356">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc19-357">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fc19-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7fc19-358">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fc19-358">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc19-359">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fc19-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7fc19-360">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7fc19-360">Namespace</span></span><br/>                | <span data-ttu-id="7fc19-361">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7fc19-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7fc19-362">MOF</span><span class="sxs-lookup"><span data-stu-id="7fc19-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fc19-363"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fc19-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fc19-364">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc19-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fc19-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fc19-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7fc19-366">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fc19-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc19-367">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7fc19-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="7fc19-368">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="7fc19-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

