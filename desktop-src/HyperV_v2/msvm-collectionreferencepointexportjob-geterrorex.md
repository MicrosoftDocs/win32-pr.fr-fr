---
description: Récupère des informations supplémentaires sur une erreur.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Méthode GetErrorEx de la classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542996"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="e0916-103">Méthode GetErrorEx de la \_ classe CollectionReferencePointExportJob MSVM</span><span class="sxs-lookup"><span data-stu-id="e0916-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="e0916-104">Récupère des informations supplémentaires sur une erreur.</span><span class="sxs-lookup"><span data-stu-id="e0916-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="e0916-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, **GetErrorEx** ne retourne aucune instance d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="e0916-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="e0916-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, **GetErrorEx** retourne une ou plusieurs instances d' **\_ erreur MSVM** .</span><span class="sxs-lookup"><span data-stu-id="e0916-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0916-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0916-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="e0916-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0916-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0916-109">*Erreurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e0916-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0916-110">Si l’état opérationnel du travail n’est pas « OK », ce paramètre retourne un tableau d’instances d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="e0916-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="e0916-111">Dans le cas contraire, si le travail est « OK », ce paramètre contient la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e0916-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0916-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0916-112">Return value</span></span>

<span data-ttu-id="e0916-113">En cas de réussite, retourne 0 ; Sinon, retourne l’une des valeurs d’erreur suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0916-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="e0916-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="e0916-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="e0916-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="e0916-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="e0916-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="e0916-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="e0916-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="e0916-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="e0916-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="e0916-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="e0916-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e0916-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e0916-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="e0916-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e0916-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0916-126">Requirements</span></span>



| <span data-ttu-id="e0916-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0916-127">Requirement</span></span> | <span data-ttu-id="e0916-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0916-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0916-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0916-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e0916-130">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0916-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e0916-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0916-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e0916-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e0916-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e0916-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0916-133">Namespace</span></span><br/>                | <span data-ttu-id="e0916-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e0916-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e0916-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e0916-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0916-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0916-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0916-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e0916-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0916-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0916-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e0916-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0916-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0916-140">**MSVM \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="e0916-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




