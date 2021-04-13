---
description: Détruisez un instantané de système virtuel existant. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Méthode DestroySnapshot de la classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526775"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="0d087-104">Méthode DestroySnapshot de la \_ classe CIM VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="0d087-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="0d087-105">Détruisez un instantané de système virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="0d087-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="0d087-106">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.</span><span class="sxs-lookup"><span data-stu-id="0d087-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d087-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d087-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0d087-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d087-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d087-109">*AffectedSnapshot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d087-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d087-110">Référence [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à l’instantané du système virtuel affecté.</span><span class="sxs-lookup"><span data-stu-id="0d087-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d087-111">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0d087-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d087-112">Si l’opération est exécutée à long terme, éventuellement [**un \_ ConcreteJob CIM**](cim-concretejob.md) représentant le travail peut être retourné.</span><span class="sxs-lookup"><span data-stu-id="0d087-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="0d087-113">Ce paramètre a été en lecture/écriture dans Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="0d087-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d087-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d087-114">Return value</span></span>

<span data-ttu-id="0d087-115">Retourne 0 en cas de réussite ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="0d087-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d087-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0d087-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-117">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0d087-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-118">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="0d087-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-119">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="0d087-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-120">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="0d087-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-121">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="0d087-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-122">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="0d087-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-123">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0d087-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-124">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0d087-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-125">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0d087-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0d087-126">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0d087-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0d087-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d087-127">Requirements</span></span>



| <span data-ttu-id="0d087-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d087-128">Requirement</span></span> | <span data-ttu-id="0d087-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d087-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d087-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d087-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d087-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0d087-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0d087-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d087-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d087-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0d087-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0d087-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d087-134">Namespace</span></span><br/>                | <span data-ttu-id="0d087-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d087-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d087-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0d087-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d087-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d087-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d087-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0d087-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d087-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d087-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d087-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d087-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d087-141">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0d087-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




