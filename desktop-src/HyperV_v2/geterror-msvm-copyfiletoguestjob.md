---
description: 'Msvm_CopyFileToGuestJob :: GetError, méthode-récupère l’objet d’erreur pour le travail, s’il en existe un.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: 'Msvm_CopyFileToGuestJob :: GetError, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119367"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="c7f8f-103">MSVM \_ CopyFileToGuestJob :: GetError, méthode</span><span class="sxs-lookup"><span data-stu-id="c7f8f-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="c7f8f-104">Récupère l’objet d’erreur pour le travail, s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="c7f8f-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="c7f8f-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne pas d’objet d' [**\_ erreur CIM**](/previous-versions//cc150671(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c7f8f-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="c7f8f-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une instance d' **\_ erreur CIM** est retournée.</span><span class="sxs-lookup"><span data-stu-id="c7f8f-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7f8f-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="c7f8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7f8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7f8f-109">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7f8f-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7f8f-110">Si l’état opérationnel du travail n’est pas 2 (OK), cette méthode retourne une instance incorporée de la classe d' [**\_ erreur MSVM**](msvm-error.md) , au format CIM-XML.</span><span class="sxs-lookup"><span data-stu-id="c7f8f-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="c7f8f-111">Si l’état opérationnel du travail est 2 (OK), la **valeur null** est retournée.</span><span class="sxs-lookup"><span data-stu-id="c7f8f-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7f8f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7f8f-112">Return value</span></span>

<span data-ttu-id="c7f8f-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c7f8f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c7f8f-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c7f8f-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c7f8f-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c7f8f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7f8f-126">Requirements</span></span>



| <span data-ttu-id="c7f8f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7f8f-127">Requirement</span></span> | <span data-ttu-id="c7f8f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7f8f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f8f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7f8f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f8f-130">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7f8f-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c7f8f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7f8f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f8f-132">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7f8f-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7f8f-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7f8f-133">Namespace</span></span><br/>                | <span data-ttu-id="c7f8f-134">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c7f8f-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="c7f8f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c7f8f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7f8f-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7f8f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7f8f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7f8f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7f8f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7f8f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7f8f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7f8f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f8f-140">**MSVM \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="c7f8f-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

