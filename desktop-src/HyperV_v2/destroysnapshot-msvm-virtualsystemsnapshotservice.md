---
description: Détruit un instantané d’ordinateur virtuel existant.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Méthode DestroySnapshot de la classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868230"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="0f7f8-103">Méthode DestroySnapshot de la \_ classe VirtualSystemSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="0f7f8-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="0f7f8-104">Détruit un instantané d’ordinateur virtuel existant.</span><span class="sxs-lookup"><span data-stu-id="0f7f8-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="0f7f8-105">Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui sont dépendants de l’instantané affecté.</span><span class="sxs-lookup"><span data-stu-id="0f7f8-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7f8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f7f8-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f7f8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f7f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f7f8-108">*AffectedSnapshot* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f7f8-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7f8-109">Référence [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) qui représente la capture instantanée d’ordinateur virtuel à détruire.</span><span class="sxs-lookup"><span data-stu-id="0f7f8-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="0f7f8-110">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0f7f8-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f7f8-111">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0f7f8-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f7f8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f7f8-112">Return value</span></span>

<span data-ttu-id="0f7f8-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0f7f8-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0f7f8-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-120">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-123">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0f7f8-124">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0f7f8-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0f7f8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f7f8-125">Requirements</span></span>



| <span data-ttu-id="0f7f8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f7f8-126">Requirement</span></span> | <span data-ttu-id="0f7f8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f7f8-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7f8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f7f8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0f7f8-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f7f8-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f7f8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f7f8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0f7f8-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f7f8-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f7f8-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0f7f8-132">Namespace</span></span><br/>                | <span data-ttu-id="0f7f8-133">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f7f8-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f7f8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0f7f8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f7f8-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f7f8-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f7f8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0f7f8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f7f8-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f7f8-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f7f8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f7f8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f7f8-139">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="0f7f8-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="0f7f8-140">**RemoveVirtualSystemSnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="0f7f8-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

