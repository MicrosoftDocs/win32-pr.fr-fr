---
title: Énumération VMVMState (VPCCOMInterfaces. h)
description: Spécifie l’état d’un ordinateur virtuel.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- Virtual PC de l’énumération VMVMState
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510171"
---
# <a name="vmvmstate-enumeration"></a><span data-ttu-id="e3ee3-104">Énumération VMVMState</span><span class="sxs-lookup"><span data-stu-id="e3ee3-104">VMVMState enumeration</span></span>

<span data-ttu-id="e3ee3-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e3ee3-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e3ee3-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e3ee3-107">Spécifie l’état d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-107">Specifies the state of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ee3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3ee3-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a><span data-ttu-id="e3ee3-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="e3ee3-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e3ee3-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-110"><span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-111">Un État non valide (ne doit pas se produire si la machine virtuelle existe).</span><span class="sxs-lookup"><span data-stu-id="e3ee3-111">An invalid state (should not occur if the virtual machine exists).</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState \_ turnedOff**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-112"><span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**vmVMState\_TurnedOff**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-113">OFF et non enregistré.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-113">Off and not saved.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ enregistré**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-114"><span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState\_Saved**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-115">Désactivé, mais l’invité est enregistré.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-115">Off but the guest is saved.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState \_ TurningOn**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-116"><span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**vmVMState\_TurningOn**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-117">Dans le processus d’activation de.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-117">In the process of turning on.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**\_restauration vmVMState**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-118"><span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**vmVMState\_Restoring**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-119">Restauration de l’État.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-119">Restoring the state.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-120"><span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState\_Running**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-121">En cours d’exécution et non suspendu.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-121">Running and not paused.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-122"><span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState\_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-123">En cours d’exécution et suspendu.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-123">Running and paused.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**\_enregistrement vmVMState**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-124"><span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**vmVMState\_Saving**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-125">Enregistrement de l’État.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-125">Saving the state.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState \_ TurningOff**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-126"><span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**vmVMState\_TurningOff**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-127">En cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-127">In the process of turning off.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState \_ MergingDrives**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-128"><span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**vmVMState\_MergingDrives**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-129">Lors du processus de fusion des disques d’annulations.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-129">In the process of merging undo drives.</span></span>

</dd> <dt>

<span data-ttu-id="e3ee3-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState \_ DeleteMachine**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-130"><span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**vmVMState\_DeleteMachine**</span></span>
</dt> <dd>

<span data-ttu-id="e3ee3-131">Suppression de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-131">Deleting the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3ee3-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3ee3-132">Requirements</span></span>



| <span data-ttu-id="e3ee3-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3ee3-133">Requirement</span></span> | <span data-ttu-id="e3ee3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3ee3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ee3-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ee3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ee3-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3ee3-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3ee3-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ee3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ee3-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3ee3-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e3ee3-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e3ee3-139">End of client support</span></span><br/>    | <span data-ttu-id="e3ee3-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3ee3-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e3ee3-141">Produit</span><span class="sxs-lookup"><span data-stu-id="e3ee3-141">Product</span></span><br/>                  | <span data-ttu-id="e3ee3-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e3ee3-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e3ee3-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3ee3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3ee3-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ee3-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ee3-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ee3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ee3-146">**IVMVirtualMachine :: State**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-146">**IVMVirtualMachine::State**</span></span>](ivmvirtualmachine-state.md)
</dt> <dt>

[<span data-ttu-id="e3ee3-147">**IVMVirtualMachineEvents :: OnStateChange**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-147">**IVMVirtualMachineEvents::OnStateChange**</span></span>](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[<span data-ttu-id="e3ee3-148">**IVMVirtualPCEvents::OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="e3ee3-148">**IVMVirtualPCEvents::OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

