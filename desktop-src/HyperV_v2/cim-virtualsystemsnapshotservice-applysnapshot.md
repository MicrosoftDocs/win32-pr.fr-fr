---
description: Applique un instantané de système virtuel au système virtuel à partir duquel il a été créé.
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: Méthode ApplySnapshot de la classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536527"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="4a5ad-103">Méthode ApplySnapshot de la \_ classe CIM VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="4a5ad-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="4a5ad-104">Applique un instantané de système virtuel au système virtuel à partir duquel il a été créé.</span><span class="sxs-lookup"><span data-stu-id="4a5ad-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a5ad-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4a5ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a5ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a5ad-107">*Instantané* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a5ad-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5ad-108">Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à l’instantané du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="4a5ad-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="4a5ad-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a5ad-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a5ad-110">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="4a5ad-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="4a5ad-111">Ce paramètre a été en lecture/écriture dans Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4a5ad-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a5ad-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a5ad-112">Return value</span></span>

<span data-ttu-id="4a5ad-113">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="4a5ad-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4a5ad-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-120">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-123">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4a5ad-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4a5ad-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4a5ad-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a5ad-125">Requirements</span></span>



| <span data-ttu-id="4a5ad-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a5ad-126">Requirement</span></span> | <span data-ttu-id="4a5ad-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a5ad-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a5ad-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a5ad-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4a5ad-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4a5ad-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4a5ad-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a5ad-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4a5ad-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4a5ad-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4a5ad-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4a5ad-132">Namespace</span></span><br/>                | <span data-ttu-id="4a5ad-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a5ad-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4a5ad-134">MOF</span><span class="sxs-lookup"><span data-stu-id="4a5ad-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a5ad-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ad-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a5ad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4a5ad-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a5ad-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a5ad-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a5ad-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a5ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a5ad-139">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4a5ad-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




