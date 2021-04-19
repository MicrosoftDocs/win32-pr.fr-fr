---
description: Supprime le point de référence spécifié.
ms.assetid: cb5245b6-5984-40ec-a37e-e4a0a62e318a
title: Méthode DestroyReferencePoint de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cf7a21e60369a928cc1d617e24db5f5fc70c522
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538259"
---
# <a name="destroyreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="50b39-103">Méthode DestroyReferencePoint de la \_ classe VirtualSystemReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="50b39-103">DestroyReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="50b39-104">Supprime le point de référence spécifié.</span><span class="sxs-lookup"><span data-stu-id="50b39-104">Deletes the specified reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50b39-105">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="50b39-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50b39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b39-107">*AffectedReferencePoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50b39-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50b39-108">Référence à l’instance [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente le point de référence à supprimer.</span><span class="sxs-lookup"><span data-stu-id="50b39-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="50b39-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50b39-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50b39-110">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="50b39-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="50b39-111">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="50b39-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b39-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50b39-112">Return value</span></span>

<span data-ttu-id="50b39-113">En cas de réussite, retourne 0 (terminé sans erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="50b39-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="50b39-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="50b39-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="50b39-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="50b39-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="50b39-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="50b39-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="50b39-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="50b39-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="50b39-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="50b39-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="50b39-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="50b39-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="50b39-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="50b39-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="50b39-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50b39-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50b39-127">Requirements</span></span>



| <span data-ttu-id="50b39-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50b39-128">Requirement</span></span> | <span data-ttu-id="50b39-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="50b39-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b39-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50b39-130">Minimum supported client</span></span><br/> | <span data-ttu-id="50b39-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50b39-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="50b39-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50b39-132">Minimum supported server</span></span><br/> | <span data-ttu-id="50b39-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="50b39-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="50b39-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="50b39-134">Namespace</span></span><br/>                | <span data-ttu-id="50b39-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="50b39-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50b39-136">MOF</span><span class="sxs-lookup"><span data-stu-id="50b39-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50b39-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50b39-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50b39-138">DLL</span><span class="sxs-lookup"><span data-stu-id="50b39-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50b39-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50b39-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50b39-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b39-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b39-141">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="50b39-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




