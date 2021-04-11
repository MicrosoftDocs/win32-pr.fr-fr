---
description: Supprime l’élément managé spécifié en tant que membre de l’élément CIM \_ CollectionOfMSEs avec l’identificateur donné. Cela échoue même si l’objet avec cet identificateur n’est pas présent.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Méthode RemoveMemberById de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210947"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="bc830-104">Méthode RemoveMemberById de la \_ classe CollectionManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="bc830-104">RemoveMemberById method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="bc830-105">Supprime l’élément managé spécifié en tant que membre de l’élément [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) avec l’identificateur donné.</span><span class="sxs-lookup"><span data-stu-id="bc830-105">Removes the specified managed element as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="bc830-106">Cela échoue même si l’objet avec cet identificateur n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="bc830-106">This will succeed even if the object with that identifier is not present.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc830-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc830-107">Syntax</span></span>


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bc830-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc830-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc830-109">*Membre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc830-109">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc830-110">Membre à supprimer.</span><span class="sxs-lookup"><span data-stu-id="bc830-110">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="bc830-111">L’un des  \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc830-111">*CollectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc830-112">ID de collection de la collection dont le membre doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="bc830-112">The collection ID of the collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="bc830-113">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc830-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc830-114">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="bc830-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc830-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc830-115">Return value</span></span>

<span data-ttu-id="bc830-116">Retourne 0 en cas de réussite, ou 4096 si le travail a démarré ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="bc830-116">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bc830-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="bc830-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="bc830-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="bc830-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="bc830-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="bc830-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="bc830-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="bc830-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="bc830-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="bc830-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="bc830-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="bc830-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="bc830-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="bc830-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bc830-130">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="bc830-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc830-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc830-131">Requirements</span></span>



| <span data-ttu-id="bc830-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc830-132">Requirement</span></span> | <span data-ttu-id="bc830-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc830-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc830-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc830-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bc830-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc830-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bc830-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc830-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bc830-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bc830-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bc830-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bc830-138">Namespace</span></span><br/>                | <span data-ttu-id="bc830-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc830-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc830-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bc830-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc830-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc830-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc830-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bc830-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc830-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc830-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc830-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc830-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc830-145">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="bc830-145">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




