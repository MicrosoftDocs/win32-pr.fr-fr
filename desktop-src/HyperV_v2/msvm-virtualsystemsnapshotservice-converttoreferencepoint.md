---
description: Convertit un instantané de système virtuel existant en un point de référence. L’instantané est supprimé comme un effet secondaire. Seuls les instantanés de récupération peuvent être convertis en points de référence.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Méthode ConvertToReferencePoint de la classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519255"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="fe05d-105">Méthode ConvertToReferencePoint de la \_ classe VirtualSystemSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="fe05d-105">ConvertToReferencePoint method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="fe05d-106">Convertit un instantané de système virtuel existant en un point de référence.</span><span class="sxs-lookup"><span data-stu-id="fe05d-106">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="fe05d-107">L’instantané est supprimé comme un effet secondaire.</span><span class="sxs-lookup"><span data-stu-id="fe05d-107">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="fe05d-108">Seuls les instantanés de récupération peuvent être convertis en points de référence.</span><span class="sxs-lookup"><span data-stu-id="fe05d-108">Only recovery snapshots can be converted to reference points.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe05d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe05d-109">Syntax</span></span>


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fe05d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe05d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe05d-111">*AffectedSnapshot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe05d-111">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe05d-112">Référence à l’instantané du système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="fe05d-112">Reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="fe05d-113">*ReferencePointSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe05d-113">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe05d-114">Paramètres.</span><span class="sxs-lookup"><span data-stu-id="fe05d-114">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="fe05d-115">*ResultingReferencePoint* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fe05d-115">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe05d-116">Point de référence du système virtuel résultant</span><span class="sxs-lookup"><span data-stu-id="fe05d-116">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="fe05d-117">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fe05d-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe05d-118">Si l’opération est exécutée à long terme, vous pouvez éventuellement retourner un travail.</span><span class="sxs-lookup"><span data-stu-id="fe05d-118">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe05d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe05d-119">Return value</span></span>

<span data-ttu-id="fe05d-120">Retourne 0 en cas de réussite ; Sinon, retourne l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe05d-120">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="fe05d-121">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fe05d-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-122">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="fe05d-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-123">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="fe05d-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-124">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="fe05d-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-125">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="fe05d-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-126">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="fe05d-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-127">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="fe05d-127">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-128">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="fe05d-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-129">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fe05d-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-130">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="fe05d-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fe05d-131">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fe05d-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fe05d-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe05d-132">Requirements</span></span>



| <span data-ttu-id="fe05d-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe05d-133">Requirement</span></span> | <span data-ttu-id="fe05d-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe05d-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe05d-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe05d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fe05d-136">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe05d-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fe05d-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe05d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fe05d-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe05d-138">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fe05d-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fe05d-139">Namespace</span></span><br/>                | <span data-ttu-id="fe05d-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fe05d-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fe05d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fe05d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe05d-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe05d-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe05d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fe05d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe05d-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe05d-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fe05d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe05d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe05d-146">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="fe05d-146">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




