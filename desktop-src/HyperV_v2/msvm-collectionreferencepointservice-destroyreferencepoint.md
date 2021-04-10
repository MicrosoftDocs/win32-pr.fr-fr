---
description: Détruit une collection de points de référence existante. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres points de référence qui dépendent de la collection de points de référence affectés.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Méthode DestroyReferencePoint de la classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115899"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="fb06c-104">Méthode DestroyReferencePoint de la \_ classe CollectionReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="fb06c-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="fb06c-105">Détruit une collection de points de référence existante.</span><span class="sxs-lookup"><span data-stu-id="fb06c-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="fb06c-106">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres points de référence qui dépendent de la collection de points de référence affectés.</span><span class="sxs-lookup"><span data-stu-id="fb06c-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb06c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb06c-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fb06c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb06c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb06c-109">*AffectedReferencePointCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb06c-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb06c-110">Référence à la collection de points de référence système virtuelle affectée.</span><span class="sxs-lookup"><span data-stu-id="fb06c-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="fb06c-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb06c-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb06c-112">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="fb06c-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb06c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb06c-113">Return value</span></span>

<span data-ttu-id="fb06c-114">En cas de réussite, retourne 0 (aucune erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="fb06c-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="fb06c-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fb06c-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-116">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="fb06c-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-117">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="fb06c-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-118">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="fb06c-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-119">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="fb06c-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-120">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="fb06c-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-121">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="fb06c-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-122">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fb06c-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-123">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fb06c-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-124">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fb06c-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fb06c-125">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fb06c-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fb06c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb06c-126">Requirements</span></span>



| <span data-ttu-id="fb06c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb06c-127">Requirement</span></span> | <span data-ttu-id="fb06c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb06c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb06c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb06c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb06c-130">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb06c-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fb06c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb06c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb06c-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fb06c-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fb06c-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fb06c-133">Namespace</span></span><br/>                | <span data-ttu-id="fb06c-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fb06c-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fb06c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fb06c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb06c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb06c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb06c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fb06c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb06c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb06c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb06c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb06c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb06c-140">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="fb06c-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




