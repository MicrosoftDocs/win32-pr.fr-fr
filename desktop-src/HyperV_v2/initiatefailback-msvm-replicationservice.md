---
description: Lance la restauration automatique pour un ordinateur virtuel de récupération.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Msvm_ReplicationService :: InitiateFailback, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524113"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="44f91-103">MSVM \_ ReplicationService :: InitiateFailback, méthode</span><span class="sxs-lookup"><span data-stu-id="44f91-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="44f91-104">Lance la restauration automatique pour un ordinateur virtuel de récupération.</span><span class="sxs-lookup"><span data-stu-id="44f91-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44f91-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="44f91-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f91-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44f91-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44f91-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel lancer une restauration automatique.</span><span class="sxs-lookup"><span data-stu-id="44f91-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="44f91-109">*ReplicationSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44f91-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44f91-110">Représentation sous forme de chaîne d’une instance incorporée de la classe [**MSVM \_ ReplicationSettingData**](msvm-replicationsettingdata.md) qui définit les paramètres de réplication pour la restauration automatique.</span><span class="sxs-lookup"><span data-stu-id="44f91-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="44f91-111">*RecoveryPointIdentifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44f91-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44f91-112">Entrée facultative qui identifie le point de récupération sur lequel la restauration automatique est demandée.</span><span class="sxs-lookup"><span data-stu-id="44f91-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="44f91-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="44f91-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44f91-114">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44f91-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="44f91-115">Cette référence peut être utilisée pour surveiller la progression et pour obtenir le résultat de la méthode.</span><span class="sxs-lookup"><span data-stu-id="44f91-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f91-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44f91-116">Return value</span></span>

<span data-ttu-id="44f91-117">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="44f91-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="44f91-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="44f91-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="44f91-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="44f91-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="44f91-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="44f91-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="44f91-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="44f91-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="44f91-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="44f91-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="44f91-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="44f91-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="44f91-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="44f91-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="44f91-131">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="44f91-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="44f91-132">Notes</span><span class="sxs-lookup"><span data-stu-id="44f91-132">Remarks</span></span>

<span data-ttu-id="44f91-133">**InitiateFailback** fonctionne sur une machine virtuelle de récupération et prend l’ordinateur virtuel à l’état *WaitingForFailback* .</span><span class="sxs-lookup"><span data-stu-id="44f91-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="44f91-134">**InitiateFailback** transmet la requête de restauration automatique au fournisseur correspondant, qui resynchronise le point de récupération du nouveau côté principal.</span><span class="sxs-lookup"><span data-stu-id="44f91-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="44f91-135">Une fois la restauration automatique du point de récupération demandé terminée, l’état de réplication passe à l’état *FailbackCompleted* .</span><span class="sxs-lookup"><span data-stu-id="44f91-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f91-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44f91-136">Requirements</span></span>



| <span data-ttu-id="44f91-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44f91-137">Requirement</span></span> | <span data-ttu-id="44f91-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="44f91-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f91-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f91-139">Minimum supported client</span></span><br/> | <span data-ttu-id="44f91-140">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44f91-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="44f91-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f91-141">Minimum supported server</span></span><br/> | <span data-ttu-id="44f91-142">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44f91-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="44f91-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="44f91-143">Namespace</span></span><br/>                | <span data-ttu-id="44f91-144">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="44f91-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="44f91-145">MOF</span><span class="sxs-lookup"><span data-stu-id="44f91-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44f91-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44f91-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44f91-147">DLL</span><span class="sxs-lookup"><span data-stu-id="44f91-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44f91-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44f91-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44f91-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44f91-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f91-150">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="44f91-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

