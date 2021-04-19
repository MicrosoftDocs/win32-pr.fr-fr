---
description: Supprime un instantané existant, ainsi que tous ses enfants, d’un ordinateur virtuel.
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Méthode DestroySnapshotTree de la classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5658e954766531765c47f8bef80d5509f2ad27c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521866"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="fbf27-103">Méthode DestroySnapshotTree de la \_ classe VirtualSystemSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="fbf27-103">DestroySnapshotTree method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="fbf27-104">Supprime un instantané existant, ainsi que tous ses enfants, d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="fbf27-104">Removes an existing snapshot, and all its children, of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf27-105">Syntax</span></span>


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fbf27-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbf27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf27-107">*SnapshotSettingData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbf27-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf27-108">Référence [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) qui représente l’arborescence des captures instantanées d’ordinateur virtuel à détruire.</span><span class="sxs-lookup"><span data-stu-id="fbf27-108">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot tree to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="fbf27-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbf27-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf27-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf27-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf27-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbf27-111">Return value</span></span>

<span data-ttu-id="fbf27-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fbf27-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fbf27-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf27-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-114">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="fbf27-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-115">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="fbf27-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-116">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="fbf27-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-117">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="fbf27-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-118">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="fbf27-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-119">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="fbf27-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-120">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="fbf27-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-121">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="fbf27-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-122">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="fbf27-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-123">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="fbf27-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-124">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="fbf27-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fbf27-125">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="fbf27-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fbf27-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbf27-126">Requirements</span></span>



| <span data-ttu-id="fbf27-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf27-127">Requirement</span></span> | <span data-ttu-id="fbf27-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf27-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf27-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf27-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf27-130">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf27-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbf27-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbf27-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf27-132">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbf27-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbf27-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbf27-133">Namespace</span></span><br/>                | <span data-ttu-id="fbf27-134">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="fbf27-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbf27-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf27-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf27-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf27-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf27-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf27-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf27-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbf27-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbf27-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf27-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf27-140">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="fbf27-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="fbf27-141">**RemoveVirtualSystemSnapshotTree (v1)**</span><span class="sxs-lookup"><span data-stu-id="fbf27-141">**RemoveVirtualSystemSnapshotTree (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

