---
description: Récupère une erreur.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Méthode GetError de la classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035130"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="619c1-103">Méthode GetError de la \_ classe CollectionReferencePointExportJob MSVM</span><span class="sxs-lookup"><span data-stu-id="619c1-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="619c1-104">Récupère une erreur.</span><span class="sxs-lookup"><span data-stu-id="619c1-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="619c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="619c1-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="619c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="619c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619c1-107">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="619c1-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="619c1-108">En cas de réussite, contient une description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="619c1-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619c1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="619c1-109">Return value</span></span>

<span data-ttu-id="619c1-110">0 en cas de réussite ; Sinon, une erreur.</span><span class="sxs-lookup"><span data-stu-id="619c1-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="619c1-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="619c1-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-112">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="619c1-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-113">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="619c1-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-114">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="619c1-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-115">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="619c1-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-116">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="619c1-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-117">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="619c1-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-118">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="619c1-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-119">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="619c1-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-120">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="619c1-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-121">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="619c1-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="619c1-122">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="619c1-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="619c1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="619c1-123">Requirements</span></span>



| <span data-ttu-id="619c1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="619c1-124">Requirement</span></span> | <span data-ttu-id="619c1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="619c1-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619c1-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="619c1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="619c1-127">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="619c1-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="619c1-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="619c1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="619c1-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="619c1-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="619c1-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="619c1-130">Namespace</span></span><br/>                | <span data-ttu-id="619c1-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="619c1-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="619c1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="619c1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="619c1-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="619c1-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="619c1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="619c1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="619c1-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="619c1-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="619c1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="619c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619c1-137">**MSVM \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="619c1-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




