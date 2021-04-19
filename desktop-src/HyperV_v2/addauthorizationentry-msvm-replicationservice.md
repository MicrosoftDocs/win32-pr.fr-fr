---
description: Ajoute une entrée d’autorisation à un serveur de récupération.
ms.assetid: edc11c5b-b1a1-45e0-a920-2f1f1b0b8779
title: Méthode AddAuthorizationEntry de la classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.AddAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fd4c47bd4468d5804ec7e096d35db271726c92b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517861"
---
# <a name="addauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="efa9f-103">Méthode AddAuthorizationEntry de la \_ classe ReplicationService MSVM</span><span class="sxs-lookup"><span data-stu-id="efa9f-103">AddAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="efa9f-104">Ajoute une entrée d’autorisation à un serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="efa9f-104">Adds an authorization entry to a recovery server.</span></span> <span data-ttu-id="efa9f-105">Ces entrées sont utilisées pour autoriser les connexions au serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="efa9f-105">These entries are used for authorizing connections to the recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa9f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efa9f-106">Syntax</span></span>


```mof
uint32 AddAuthorizationEntry(
  [in]  string              AuthorizationEntry,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="efa9f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efa9f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efa9f-108">*AuthorizationEntry* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="efa9f-108">*AuthorizationEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa9f-109">Représentation sous forme de chaîne d’une instance de la classe [**MSVM \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) qui définit l’entrée d’autorisation à ajouter.</span><span class="sxs-lookup"><span data-stu-id="efa9f-109">A string representation of an instance of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class that defines the authorization entry to be added.</span></span>

</dd> <dt>

<span data-ttu-id="efa9f-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="efa9f-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efa9f-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="efa9f-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efa9f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="efa9f-112">Return value</span></span>

<span data-ttu-id="efa9f-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="efa9f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="efa9f-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="efa9f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="efa9f-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="efa9f-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="efa9f-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="efa9f-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="efa9f-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="efa9f-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="efa9f-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="efa9f-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="efa9f-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="efa9f-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="efa9f-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="efa9f-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="efa9f-127">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="efa9f-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="efa9f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efa9f-128">Requirements</span></span>



| <span data-ttu-id="efa9f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efa9f-129">Requirement</span></span> | <span data-ttu-id="efa9f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="efa9f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa9f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efa9f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="efa9f-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efa9f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="efa9f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efa9f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="efa9f-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="efa9f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="efa9f-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="efa9f-135">Namespace</span></span><br/>                | <span data-ttu-id="efa9f-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="efa9f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="efa9f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="efa9f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efa9f-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efa9f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efa9f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="efa9f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efa9f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efa9f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efa9f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efa9f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efa9f-142">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="efa9f-142">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="efa9f-143">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="efa9f-143">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="efa9f-144">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="efa9f-144">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="efa9f-145">**MSVM \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="efa9f-145">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

