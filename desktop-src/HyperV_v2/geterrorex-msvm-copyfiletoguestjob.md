---
description: Récupère les objets d’erreur pour le travail, le cas échéant.
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: 'Msvm_CopyFileToGuestJob :: GetErrorEx, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 179ad3a70a985442d855d447ef4eab955d177f0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514643"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="9f4e8-103">MSVM \_ CopyFileToGuestJob :: GetErrorEx, méthode</span><span class="sxs-lookup"><span data-stu-id="9f4e8-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="9f4e8-104">Récupère les objets d’erreur pour le travail, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="9f4e8-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="9f4e8-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="9f4e8-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="9f4e8-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une ou plusieurs instances d' **\_ erreur MSVM** sont retournées.</span><span class="sxs-lookup"><span data-stu-id="9f4e8-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f4e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f4e8-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="9f4e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f4e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f4e8-109">*Erreurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9f4e8-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f4e8-110">Si l’état opérationnel du travail n’est pas 2 (OK), cette méthode retourne une ou plusieurs instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) , au format CIM-XML, qui représentent les erreurs rencontrées dans le travail.</span><span class="sxs-lookup"><span data-stu-id="9f4e8-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="9f4e8-111">Si l’état opérationnel du travail est 2 (OK), la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="9f4e8-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f4e8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f4e8-112">Return value</span></span>

<span data-ttu-id="9f4e8-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9f4e8-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9f4e8-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9f4e8-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="9f4e8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9f4e8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f4e8-126">Requirements</span></span>



| <span data-ttu-id="9f4e8-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f4e8-127">Requirement</span></span> | <span data-ttu-id="9f4e8-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f4e8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f4e8-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f4e8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f4e8-130">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f4e8-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9f4e8-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f4e8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f4e8-132">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f4e8-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f4e8-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9f4e8-133">Namespace</span></span><br/>                | <span data-ttu-id="9f4e8-134">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f4e8-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="9f4e8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9f4e8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f4e8-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f4e8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f4e8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9f4e8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f4e8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f4e8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f4e8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f4e8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f4e8-140">**MSVM \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="9f4e8-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




