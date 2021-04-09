---
description: Applique un instantané d’ordinateur virtuel à la machine virtuelle à partir de laquelle il a été créé.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Méthode ApplySnapshot de la classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865222"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="79572-103">Méthode ApplySnapshot de la \_ classe VirtualSystemSnapshotService MSVM</span><span class="sxs-lookup"><span data-stu-id="79572-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="79572-104">Applique un instantané d’ordinateur virtuel à la machine virtuelle à partir de laquelle il a été créé.</span><span class="sxs-lookup"><span data-stu-id="79572-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="79572-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79572-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="79572-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79572-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79572-107">*Instantané* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79572-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79572-108">Référence à une classe dérivée de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) qui représente la capture instantanée d’ordinateur virtuel à appliquer.</span><span class="sxs-lookup"><span data-stu-id="79572-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="79572-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79572-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79572-110">Cette opération est toujours exécutée de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="79572-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="79572-111">Cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79572-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79572-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79572-112">Return value</span></span>

<span data-ttu-id="79572-113">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="79572-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="79572-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="79572-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79572-115">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="79572-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79572-116">**Échec** (2)</span><span class="sxs-lookup"><span data-stu-id="79572-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79572-117">**Délai d’expiration** (3)</span><span class="sxs-lookup"><span data-stu-id="79572-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79572-118">**Paramètre non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="79572-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79572-119">**État non valide** (5)</span><span class="sxs-lookup"><span data-stu-id="79572-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79572-120">**Type non valide** (6)</span><span class="sxs-lookup"><span data-stu-id="79572-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79572-121">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="79572-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79572-122">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="79572-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="79572-123">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="79572-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="79572-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="79572-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="79572-125">**État non valide** (32775)</span><span class="sxs-lookup"><span data-stu-id="79572-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="79572-126">**Méthode réservée** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="79572-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="79572-127">**Spécifique au fournisseur** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="79572-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="79572-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79572-128">Requirements</span></span>



| <span data-ttu-id="79572-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79572-129">Requirement</span></span> | <span data-ttu-id="79572-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="79572-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79572-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79572-131">Minimum supported client</span></span><br/> | <span data-ttu-id="79572-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79572-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="79572-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79572-133">Minimum supported server</span></span><br/> | <span data-ttu-id="79572-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79572-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79572-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="79572-135">Namespace</span></span><br/>                | <span data-ttu-id="79572-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="79572-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="79572-137">MOF</span><span class="sxs-lookup"><span data-stu-id="79572-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79572-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79572-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79572-139">DLL</span><span class="sxs-lookup"><span data-stu-id="79572-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79572-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79572-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79572-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79572-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79572-142">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="79572-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="79572-143">**ApplyVirtualSystemSnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="79572-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="79572-144">**ApplyVirtualSystemSnapshotEx (v1)**</span><span class="sxs-lookup"><span data-stu-id="79572-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

