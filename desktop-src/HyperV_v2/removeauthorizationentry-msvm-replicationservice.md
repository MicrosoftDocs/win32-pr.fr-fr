---
description: Supprime une entrée d’autorisation d’un serveur de récupération.
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Méthode RemoveAuthorizationEntry de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535598"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="bb771-103">Méthode RemoveAuthorizationEntry de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="bb771-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="bb771-104">Supprime une entrée d’autorisation d’un serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="bb771-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb771-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb771-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bb771-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb771-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb771-107">*AllowedPrimaryHostSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bb771-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb771-108">Serveur principal pour lequel l’entrée d’autorisation sera supprimée du serveur.</span><span class="sxs-lookup"><span data-stu-id="bb771-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="bb771-109">C’est le même que la propriété **AllowedPrimaryHostSystem** de la classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="bb771-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="bb771-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bb771-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb771-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb771-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb771-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb771-112">Return value</span></span>

<span data-ttu-id="bb771-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bb771-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bb771-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="bb771-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="bb771-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="bb771-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="bb771-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="bb771-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="bb771-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="bb771-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="bb771-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="bb771-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="bb771-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="bb771-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bb771-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="bb771-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bb771-127">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="bb771-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bb771-128">Notes</span><span class="sxs-lookup"><span data-stu-id="bb771-128">Remarks</span></span>

<span data-ttu-id="bb771-129">La suppression d’une entrée d’autorisation entraînera l’arrêt de la réplication pour les machines virtuelles autorisées avec l’entrée.</span><span class="sxs-lookup"><span data-stu-id="bb771-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb771-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb771-130">Requirements</span></span>



| <span data-ttu-id="bb771-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb771-131">Requirement</span></span> | <span data-ttu-id="bb771-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb771-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb771-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb771-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bb771-134">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb771-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb771-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb771-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bb771-136">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bb771-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb771-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bb771-137">Namespace</span></span><br/>                | <span data-ttu-id="bb771-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb771-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bb771-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bb771-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb771-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb771-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb771-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bb771-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb771-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb771-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb771-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb771-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb771-144">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="bb771-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="bb771-145">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="bb771-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="bb771-146">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="bb771-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="bb771-147">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="bb771-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

