---
description: Supprime l’élément managé spécifié en tant que membre de l' \_ objet CIM CollectionOfMSEs donné.
ms.assetid: ea945d24-bcff-476b-9adb-c6573cdbc0b5
title: Méthode RemoveMember de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 894230dcf5e9a537ca444815f8e941a8e6fcf09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867969"
---
# <a name="removemember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="aebbf-103">Méthode RemoveMember de la \_ classe CollectionManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="aebbf-103">RemoveMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="aebbf-104">Supprime l’élément managé spécifié en tant que membre de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="aebbf-104">Removes the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aebbf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aebbf-105">Syntax</span></span>


```mof
uint32 RemoveMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="aebbf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aebbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aebbf-107">*Membre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aebbf-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebbf-108">Membre à supprimer.</span><span class="sxs-lookup"><span data-stu-id="aebbf-108">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="aebbf-109">*Collection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aebbf-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aebbf-110">Collection à partir de laquelle supprimer le membre.</span><span class="sxs-lookup"><span data-stu-id="aebbf-110">The collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="aebbf-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aebbf-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aebbf-112">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="aebbf-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aebbf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aebbf-113">Return value</span></span>

<span data-ttu-id="aebbf-114">Retourne 0 en cas de réussite, ou 4096 si le travail a démarré ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="aebbf-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="aebbf-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="aebbf-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="aebbf-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="aebbf-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="aebbf-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="aebbf-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="aebbf-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="aebbf-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="aebbf-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="aebbf-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="aebbf-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="aebbf-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="aebbf-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="aebbf-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="aebbf-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="aebbf-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aebbf-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aebbf-129">Requirements</span></span>



| <span data-ttu-id="aebbf-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aebbf-130">Requirement</span></span> | <span data-ttu-id="aebbf-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="aebbf-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aebbf-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aebbf-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aebbf-133">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aebbf-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="aebbf-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aebbf-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aebbf-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aebbf-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aebbf-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aebbf-136">Namespace</span></span><br/>                | <span data-ttu-id="aebbf-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="aebbf-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aebbf-138">MOF</span><span class="sxs-lookup"><span data-stu-id="aebbf-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aebbf-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aebbf-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aebbf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="aebbf-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aebbf-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aebbf-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aebbf-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aebbf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aebbf-143">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="aebbf-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




