---
description: Efface l’état de l’enregistrement d’un instantané existant.
ms.assetid: abb0ed4a-7f89-4d32-93d2-7491d2f2aa83
title: Méthode ClearSnapshotState de la classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ClearSnapshotState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a218b600e45d91d8c744d6b49afe97666ddb51ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544273"
---
# <a name="clearsnapshotstate-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="04e1d-103">Méthode ClearSnapshotState de la \_ classe VirtualSystemSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="04e1d-103">ClearSnapshotState method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="04e1d-104">Efface l’état de l’enregistrement d’un instantané existant.</span><span class="sxs-lookup"><span data-stu-id="04e1d-104">Clears save state from an existing snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04e1d-105">Syntax</span></span>


```mof
uint32 ClearSnapshotState(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="04e1d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04e1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e1d-107">*SnapshotSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04e1d-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04e1d-108">Référence à l’instance [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) qui représente l’instantané dont l’État doit être effacé.</span><span class="sxs-lookup"><span data-stu-id="04e1d-108">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot whose state is to be cleared.</span></span>

</dd> <dt>

<span data-ttu-id="04e1d-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04e1d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04e1d-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04e1d-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e1d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04e1d-111">Return value</span></span>

<span data-ttu-id="04e1d-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="04e1d-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="04e1d-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="04e1d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="04e1d-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="04e1d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="04e1d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="04e1d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="04e1d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="04e1d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="04e1d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="04e1d-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="04e1d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="04e1d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="04e1d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="04e1d-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="04e1d-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="04e1d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04e1d-126">Requirements</span></span>



| <span data-ttu-id="04e1d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04e1d-127">Requirement</span></span> | <span data-ttu-id="04e1d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="04e1d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e1d-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e1d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04e1d-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04e1d-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="04e1d-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04e1d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04e1d-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04e1d-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04e1d-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="04e1d-133">Namespace</span></span><br/>                | <span data-ttu-id="04e1d-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="04e1d-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="04e1d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="04e1d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04e1d-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04e1d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="04e1d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="04e1d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04e1d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04e1d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="04e1d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04e1d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e1d-140">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="04e1d-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

