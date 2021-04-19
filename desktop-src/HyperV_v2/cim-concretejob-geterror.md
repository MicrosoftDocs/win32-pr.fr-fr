---
description: Récupère une erreur en raison d’une tâche ayant échoué.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Méthode GetError de la classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516932"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="4b3ee-103">Méthode GetError de la \_ classe CIM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="4b3ee-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="4b3ee-104">Récupère une erreur en raison d’une tâche ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="4b3ee-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="4b3ee-105">Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur CIM**](cim-error.md) .</span><span class="sxs-lookup"><span data-stu-id="4b3ee-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="4b3ee-106">Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une instance d' **\_ erreur CIM** est retournée.</span><span class="sxs-lookup"><span data-stu-id="4b3ee-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b3ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b3ee-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="4b3ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b3ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b3ee-109">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b3ee-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b3ee-110">Retourne une instance d' [**\_ erreur CIM**](cim-error.md) si le **OperationalStatus** sur le travail n’est pas « OK »; sinon, retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4b3ee-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b3ee-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b3ee-111">Return value</span></span>

<span data-ttu-id="4b3ee-112">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="4b3ee-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b3ee-113">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-115">**Erreur non spécifiée** (2)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-116">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-117">**Échec** (4)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-118">**Paramètre non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-119">**Accès refusé** (6)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-120">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4b3ee-121">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4b3ee-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4b3ee-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b3ee-122">Requirements</span></span>



| <span data-ttu-id="4b3ee-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b3ee-123">Requirement</span></span> | <span data-ttu-id="4b3ee-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b3ee-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3ee-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3ee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3ee-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b3ee-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4b3ee-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b3ee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3ee-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4b3ee-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4b3ee-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b3ee-129">Namespace</span></span><br/>                | <span data-ttu-id="4b3ee-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b3ee-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b3ee-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4b3ee-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b3ee-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b3ee-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b3ee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4b3ee-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b3ee-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b3ee-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b3ee-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b3ee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3ee-136">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="4b3ee-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




