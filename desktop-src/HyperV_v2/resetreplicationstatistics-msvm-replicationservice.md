---
description: Réinitialise les statistiques de réplication pour un ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Méthode ResetReplicationStatistics de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520572"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="2181c-103">Méthode ResetReplicationStatistics de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="2181c-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2181c-104">Réinitialise les statistiques de réplication pour un ordinateur virtuel et agit sur la relation de réplication principale de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2181c-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="2181c-105">À partir de Windows 8.1, nous vous recommandons de ne pas utiliser **ResetReplicationStatistics** plus pour réinitialiser les statistiques de réplication.</span><span class="sxs-lookup"><span data-stu-id="2181c-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="2181c-106">Utilisez plutôt [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="2181c-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2181c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2181c-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2181c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2181c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2181c-109">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2181c-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2181c-110">Référence à une instance de la classe [**CIM \_ CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente l’ordinateur virtuel pour lequel réinitialiser les statistiques de réplication.</span><span class="sxs-lookup"><span data-stu-id="2181c-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="2181c-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2181c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2181c-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2181c-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2181c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2181c-113">Return value</span></span>

<span data-ttu-id="2181c-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2181c-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2181c-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="2181c-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="2181c-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="2181c-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="2181c-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="2181c-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="2181c-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="2181c-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="2181c-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="2181c-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="2181c-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="2181c-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2181c-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="2181c-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2181c-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="2181c-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2181c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2181c-129">Requirements</span></span>



| <span data-ttu-id="2181c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2181c-130">Requirement</span></span> | <span data-ttu-id="2181c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2181c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2181c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2181c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2181c-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2181c-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2181c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2181c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2181c-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2181c-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2181c-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2181c-136">Namespace</span></span><br/>                | <span data-ttu-id="2181c-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2181c-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2181c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2181c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2181c-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2181c-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2181c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2181c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2181c-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2181c-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2181c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2181c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2181c-143">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="2181c-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2181c-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="2181c-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

