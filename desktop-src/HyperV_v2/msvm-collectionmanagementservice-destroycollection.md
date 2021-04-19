---
description: Supprime l' \_ objet CIM CollectionOfMSEs donné.
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Méthode DestroyCollection de la classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529483"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="300a7-103">Méthode DestroyCollection de la \_ classe CollectionManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="300a7-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="300a7-104">Supprime l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.</span><span class="sxs-lookup"><span data-stu-id="300a7-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="300a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="300a7-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="300a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="300a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300a7-107">*Collection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="300a7-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="300a7-108">Collection à détruire.</span><span class="sxs-lookup"><span data-stu-id="300a7-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="300a7-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="300a7-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="300a7-110">Référence au travail (peut avoir la valeur null si la tâche est terminée).</span><span class="sxs-lookup"><span data-stu-id="300a7-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300a7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="300a7-111">Return value</span></span>

<span data-ttu-id="300a7-112">Retourne 0 en cas de réussite, ou 4096 si le travail a démarré ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="300a7-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="300a7-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="300a7-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="300a7-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="300a7-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="300a7-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="300a7-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="300a7-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="300a7-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="300a7-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="300a7-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="300a7-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="300a7-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="300a7-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="300a7-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="300a7-126">**Fichier introuvable** (32779)</span><span class="sxs-lookup"><span data-stu-id="300a7-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="300a7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="300a7-127">Requirements</span></span>



| <span data-ttu-id="300a7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="300a7-128">Requirement</span></span> | <span data-ttu-id="300a7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="300a7-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="300a7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="300a7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="300a7-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="300a7-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="300a7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="300a7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="300a7-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="300a7-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="300a7-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="300a7-134">Namespace</span></span><br/>                | <span data-ttu-id="300a7-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="300a7-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="300a7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="300a7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="300a7-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="300a7-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="300a7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="300a7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="300a7-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="300a7-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="300a7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="300a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300a7-141">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="300a7-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




