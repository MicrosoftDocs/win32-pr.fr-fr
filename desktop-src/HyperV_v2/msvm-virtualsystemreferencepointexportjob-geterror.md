---
description: Récupère l’erreur.
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Méthode GetError de la classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104042924"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="90c82-103">Méthode GetError de la \_ classe VirtualSystemReferencePointExportJob MSVM</span><span class="sxs-lookup"><span data-stu-id="90c82-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="90c82-104">Récupère l’erreur.</span><span class="sxs-lookup"><span data-stu-id="90c82-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90c82-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="90c82-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c82-107">*Erreur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="90c82-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90c82-108">Erreur récupérée.</span><span class="sxs-lookup"><span data-stu-id="90c82-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c82-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90c82-109">Return value</span></span>

<span data-ttu-id="90c82-110">En cas de réussite, retourne 0 ; dans le cas contraire, contient une erreur.</span><span class="sxs-lookup"><span data-stu-id="90c82-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="90c82-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="90c82-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-112">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="90c82-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-113">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="90c82-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-114">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="90c82-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-115">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="90c82-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-116">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="90c82-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-117">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="90c82-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-118">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="90c82-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-119">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="90c82-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-120">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="90c82-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-121">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="90c82-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="90c82-122">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="90c82-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="90c82-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90c82-123">Requirements</span></span>



| <span data-ttu-id="90c82-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90c82-124">Requirement</span></span> | <span data-ttu-id="90c82-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="90c82-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90c82-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90c82-126">Minimum supported client</span></span><br/> | <span data-ttu-id="90c82-127">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90c82-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90c82-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90c82-128">Minimum supported server</span></span><br/> | <span data-ttu-id="90c82-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="90c82-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="90c82-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90c82-130">Namespace</span></span><br/>                | <span data-ttu-id="90c82-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="90c82-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90c82-132">MOF</span><span class="sxs-lookup"><span data-stu-id="90c82-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90c82-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90c82-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90c82-134">DLL</span><span class="sxs-lookup"><span data-stu-id="90c82-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c82-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90c82-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90c82-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90c82-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c82-137">**MSVM \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="90c82-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




