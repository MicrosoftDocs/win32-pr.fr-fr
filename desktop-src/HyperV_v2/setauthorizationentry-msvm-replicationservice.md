---
description: Définit l’entrée d’autorisation de réplication pour un ordinateur virtuel.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: Méthode SetAuthorizationEntry de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 03b2c2c37a38e957a1b560e2314845abf204ee01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524640"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="6864b-103">Méthode SetAuthorizationEntry de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="6864b-103">SetAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="6864b-104">Définit l’entrée d’autorisation de réplication pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6864b-104">Sets the replication authorization entry for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6864b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6864b-105">Syntax</span></span>


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6864b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6864b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6864b-107">*ComputerSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6864b-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6864b-108">Référence à une instance [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) qui représente la machine virtuelle pour laquelle définir l’entrée d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="6864b-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to set the authorization entry for.</span></span>

</dd> <dt>

<span data-ttu-id="6864b-109">*AuthorizationEntry* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6864b-109">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6864b-110">Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) qui définit l’entrée d’autorisation à utiliser pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6864b-110">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be used for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6864b-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6864b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6864b-112">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6864b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6864b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6864b-113">Return value</span></span>

<span data-ttu-id="6864b-114">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6864b-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6864b-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6864b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6864b-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="6864b-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="6864b-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="6864b-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="6864b-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="6864b-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="6864b-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="6864b-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="6864b-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="6864b-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="6864b-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="6864b-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6864b-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="6864b-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6864b-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6864b-129">Requirements</span></span>



| <span data-ttu-id="6864b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6864b-130">Requirement</span></span> | <span data-ttu-id="6864b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6864b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6864b-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6864b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6864b-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6864b-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6864b-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6864b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6864b-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6864b-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6864b-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6864b-136">Namespace</span></span><br/>                | <span data-ttu-id="6864b-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6864b-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6864b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6864b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6864b-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6864b-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6864b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6864b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6864b-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6864b-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6864b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6864b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6864b-143">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="6864b-143">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6864b-144">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="6864b-144">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6864b-145">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="6864b-145">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="6864b-146">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="6864b-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

