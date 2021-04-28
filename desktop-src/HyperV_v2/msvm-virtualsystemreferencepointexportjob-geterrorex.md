---
description: 'Méthode GetErrorEx de la classe Msvm_VirtualSystemReferencePointExportJob : récupère des informations supplémentaires sur une erreur.'
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Méthode GetErrorEx de la classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80e0850018b20497dbc42bbdbb802ffe4317489b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118607"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="09282-103">Méthode GetErrorEx de la \_ classe VirtualSystemReferencePointExportJob MSVM</span><span class="sxs-lookup"><span data-stu-id="09282-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="09282-104">Récupère des informations supplémentaires sur une erreur.</span><span class="sxs-lookup"><span data-stu-id="09282-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="09282-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, **GetErrorEx** ne retourne aucune instance **GetErrorEx** .</span><span class="sxs-lookup"><span data-stu-id="09282-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="09282-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, **GetErrorEx** retourne une ou plusieurs instances d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="09282-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="09282-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09282-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="09282-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09282-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09282-109">*Erreurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="09282-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09282-110">Si l’état opérationnel du travail n’est pas « OK », ce paramètre retourne un tableau d’instances d' [**\_ erreur MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="09282-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="09282-111">Dans le cas contraire, si le travail est « OK », ce paramètre contient la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="09282-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09282-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="09282-112">Return value</span></span>

<span data-ttu-id="09282-113">En cas de réussite, retourne 0 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="09282-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="09282-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="09282-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09282-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="09282-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="09282-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="09282-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="09282-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="09282-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="09282-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="09282-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="09282-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="09282-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="09282-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="09282-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="09282-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="09282-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="09282-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="09282-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="09282-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="09282-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="09282-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="09282-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="09282-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="09282-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="09282-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09282-126">Requirements</span></span>



| <span data-ttu-id="09282-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09282-127">Requirement</span></span> | <span data-ttu-id="09282-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="09282-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09282-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09282-129">Minimum supported client</span></span><br/> | <span data-ttu-id="09282-130">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09282-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="09282-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09282-131">Minimum supported server</span></span><br/> | <span data-ttu-id="09282-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="09282-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="09282-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="09282-133">Namespace</span></span><br/>                | <span data-ttu-id="09282-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="09282-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="09282-135">MOF</span><span class="sxs-lookup"><span data-stu-id="09282-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09282-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09282-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09282-137">DLL</span><span class="sxs-lookup"><span data-stu-id="09282-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09282-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09282-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09282-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09282-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09282-140">**MSVM \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="09282-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




