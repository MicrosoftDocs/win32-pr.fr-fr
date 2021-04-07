---
description: Ajoute l’élément managé spécifié en tant que membre de l' \_ objet CIM CollectionOfMSEs donné.
ms.assetid: 6f23eecc-b445-4495-ae96-76b89652a1cb
title: Méthode AddMember de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.AddMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6b885701086262fda48c5d50abd750eca6866c72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760498"
---
# <a name="addmember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="38be1-103">Méthode AddMember de la \_ classe MSVM CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="38be1-103">AddMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="38be1-104">Ajoute l’élément managé spécifié en tant que membre de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="38be1-104">Adds the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="38be1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38be1-105">Syntax</span></span>


```mof
uint32 AddMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="38be1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38be1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38be1-107">*Membre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38be1-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38be1-108">Membre à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="38be1-108">The member to add to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="38be1-109">*Collection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38be1-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38be1-110">Collection à laquelle ajouter le membre.</span><span class="sxs-lookup"><span data-stu-id="38be1-110">The collection to add the member to.</span></span>

</dd> <dt>

<span data-ttu-id="38be1-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38be1-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38be1-112">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="38be1-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38be1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="38be1-113">Return value</span></span>

<span data-ttu-id="38be1-114">Retourne 0 en cas de réussite, ou 4096 si le travail a démarré ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="38be1-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="38be1-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="38be1-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="38be1-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="38be1-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="38be1-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="38be1-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="38be1-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="38be1-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="38be1-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="38be1-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="38be1-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="38be1-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="38be1-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="38be1-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="38be1-128">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="38be1-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="38be1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38be1-129">Requirements</span></span>



| <span data-ttu-id="38be1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38be1-130">Requirement</span></span> | <span data-ttu-id="38be1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="38be1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38be1-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38be1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="38be1-133">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="38be1-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="38be1-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38be1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="38be1-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="38be1-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="38be1-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38be1-136">Namespace</span></span><br/>                | <span data-ttu-id="38be1-137">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="38be1-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="38be1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="38be1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38be1-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38be1-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38be1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="38be1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38be1-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38be1-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38be1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38be1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38be1-143">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="38be1-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




