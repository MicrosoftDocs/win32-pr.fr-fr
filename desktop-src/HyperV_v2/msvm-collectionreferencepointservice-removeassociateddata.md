---
description: Supprime le journal de données associé au point de référence.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Méthode RemoveAssociatedData de la classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aec1ac249616c08c6abf1f156ad5a3416c8afaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541233"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="f778f-103">Méthode RemoveAssociatedData de la \_ classe CollectionReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="f778f-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="f778f-104">Supprime le journal de données associé au point de référence.</span><span class="sxs-lookup"><span data-stu-id="f778f-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="f778f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f778f-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f778f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f778f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f778f-107">*AffectedReferencePointCollection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f778f-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f778f-108">Référence à la collection de points de référence système virtuelle affectée.</span><span class="sxs-lookup"><span data-stu-id="f778f-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="f778f-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f778f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f778f-110">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="f778f-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f778f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f778f-111">Return value</span></span>

<span data-ttu-id="f778f-112">En cas de réussite, retourne 0 (aucune erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="f778f-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="f778f-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="f778f-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="f778f-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-115">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="f778f-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-116">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="f778f-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-117">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="f778f-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-118">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="f778f-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-119">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="f778f-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="f778f-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="f778f-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-122">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f778f-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f778f-123">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f778f-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f778f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f778f-124">Requirements</span></span>



| <span data-ttu-id="f778f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f778f-125">Requirement</span></span> | <span data-ttu-id="f778f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f778f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f778f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f778f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f778f-128">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f778f-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f778f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f778f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f778f-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f778f-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f778f-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f778f-131">Namespace</span></span><br/>                | <span data-ttu-id="f778f-132">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f778f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f778f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f778f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f778f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f778f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f778f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f778f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f778f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f778f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f778f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f778f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f778f-138">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="f778f-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




