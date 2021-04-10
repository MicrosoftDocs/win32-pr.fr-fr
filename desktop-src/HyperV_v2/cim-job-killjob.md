---
description: Méthode permettant d’arrêter ce travail et tous les processus sous-jacents, et de supprimer toute association non résolue. Cette méthode est déconseillée ; Utilisez RequestChangeState à la place.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Méthode KillJob de la classe CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951810"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="5f4e9-104">Méthode KillJob de la \_ classe Job CIM</span><span class="sxs-lookup"><span data-stu-id="5f4e9-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="5f4e9-105">Méthode permettant d’arrêter ce travail et tous les processus sous-jacents, et de supprimer toute association « non résolue ».</span><span class="sxs-lookup"><span data-stu-id="5f4e9-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="5f4e9-106">Cette méthode est déconseillée ; Utilisez **RequestChangeState** à la place.</span><span class="sxs-lookup"><span data-stu-id="5f4e9-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="5f4e9-107">**KillJob** est déconseillé, car il n’existe aucune distinction entre un arrêt ordonné et un arrêt immédiat.</span><span class="sxs-lookup"><span data-stu-id="5f4e9-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="5f4e9-108">[**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fournit les options’Terminate’et’Kill’pour permettre cette distinction.</span><span class="sxs-lookup"><span data-stu-id="5f4e9-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4e9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f4e9-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="5f4e9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f4e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4e9-111">*DeleteOnKill* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f4e9-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4e9-112">Indique si le travail doit être supprimé automatiquement lors de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="5f4e9-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="5f4e9-113">Ce paramètre est prioritaire sur la propriété **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="5f4e9-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4e9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f4e9-114">Return value</span></span>

<span data-ttu-id="5f4e9-115">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="5f4e9-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5f4e9-116">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-118">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-120">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-121">**Accès refusé** (6)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-122">**Introuvable** (7)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5f4e9-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5f4e9-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5f4e9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f4e9-125">Requirements</span></span>



| <span data-ttu-id="5f4e9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f4e9-126">Requirement</span></span> | <span data-ttu-id="5f4e9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f4e9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4e9-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f4e9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4e9-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5f4e9-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5f4e9-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f4e9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4e9-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5f4e9-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5f4e9-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f4e9-132">Namespace</span></span><br/>                | <span data-ttu-id="5f4e9-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5f4e9-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5f4e9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5f4e9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f4e9-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f4e9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f4e9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5f4e9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f4e9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f4e9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5f4e9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f4e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4e9-139">**\_Travail CIM**</span><span class="sxs-lookup"><span data-stu-id="5f4e9-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




