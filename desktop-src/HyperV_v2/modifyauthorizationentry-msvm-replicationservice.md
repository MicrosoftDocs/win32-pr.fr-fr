---
description: Modifie une entrée d’autorisation pour un serveur de récupération.
ms.assetid: fbdf3ecd-42de-49a8-85b8-51fc9c9fcf26
title: Méthode ModifyAuthorizationEntry de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 17f5ff1a0e4e1cca95dc5f7764d2f8e2bf9d2c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530655"
---
# <a name="modifyauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="2680a-103">Méthode ModifyAuthorizationEntry de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="2680a-103">ModifyAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2680a-104">Modifie une entrée d’autorisation pour un serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="2680a-104">Modifies an authorization entry for a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2680a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2680a-105">Syntax</span></span>


```mof
uint32 ModifyAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2680a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2680a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2680a-107">*AuthorizationEntry* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2680a-107">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2680a-108">Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) qui définit l’entrée d’autorisation à modifier.</span><span class="sxs-lookup"><span data-stu-id="2680a-108">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="2680a-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2680a-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2680a-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2680a-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2680a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2680a-111">Return value</span></span>

<span data-ttu-id="2680a-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2680a-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2680a-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="2680a-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="2680a-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="2680a-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="2680a-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="2680a-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="2680a-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="2680a-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="2680a-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="2680a-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="2680a-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="2680a-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2680a-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="2680a-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2680a-126">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="2680a-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2680a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2680a-127">Requirements</span></span>



| <span data-ttu-id="2680a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2680a-128">Requirement</span></span> | <span data-ttu-id="2680a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2680a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2680a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2680a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2680a-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2680a-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2680a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2680a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2680a-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2680a-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2680a-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2680a-134">Namespace</span></span><br/>                | <span data-ttu-id="2680a-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2680a-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2680a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2680a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2680a-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2680a-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2680a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2680a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2680a-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2680a-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2680a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2680a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2680a-141">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2680a-141">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2680a-142">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2680a-142">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2680a-143">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="2680a-143">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2680a-144">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="2680a-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

