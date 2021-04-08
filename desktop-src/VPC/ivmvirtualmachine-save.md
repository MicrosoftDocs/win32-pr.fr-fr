---
title: Méthode Save IVMVirtualMachine (VPCCOMInterfaces. h)
description: Enregistre l’état de l’ordinateur virtuel.
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Enregistrer la méthode Virtual PC
- Enregistrer la méthode Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b4dbe18b89f107657d67fb7e7b90e024b01383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742884"
---
# <a name="ivmvirtualmachinesave-method"></a><span data-ttu-id="da863-106">IVMVirtualMachine :: Save, méthode</span><span class="sxs-lookup"><span data-stu-id="da863-106">IVMVirtualMachine::Save method</span></span>

<span data-ttu-id="da863-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da863-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="da863-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="da863-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="da863-109">Enregistre l’état de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="da863-109">Saves the virtual machine (VM) state.</span></span>

## <a name="syntax"></a><span data-ttu-id="da863-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da863-110">Syntax</span></span>


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a><span data-ttu-id="da863-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da863-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da863-112">*saveTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="da863-112">*saveTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="da863-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence d’enregistrement de l’état de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="da863-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's state saving sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da863-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da863-114">Return value</span></span>

<span data-ttu-id="da863-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="da863-115">This method can return one of these values.</span></span>



| <span data-ttu-id="da863-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="da863-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="da863-117">Description</span><span class="sxs-lookup"><span data-stu-id="da863-117">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="da863-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="da863-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="da863-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="da863-119">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="da863-120"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="da863-120"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="da863-121">Impossible d’enregistrer la machine virtuelle, car les disques d’annulations ont été marqués pour suppression.</span><span class="sxs-lookup"><span data-stu-id="da863-121">The VM could not be saved because the undo disks were marked for deletion.</span></span><br/>    |
| <dl> <span data-ttu-id="da863-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="da863-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="da863-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="da863-123">The parameter is **NULL**.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="da863-124">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="da863-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="da863-125">L’appelant doit disposer des autorisations d’accès en exécution pour enregistrer l’état de cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="da863-125">The caller must have execute access permissions to save the state of this VM.</span></span><br/> |
| <dl> <span data-ttu-id="da863-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="da863-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="da863-127">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="da863-127">The VM is not running.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="da863-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="da863-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="da863-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="da863-129">An unexpected error has occurred.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="da863-130">Notes</span><span class="sxs-lookup"><span data-stu-id="da863-130">Remarks</span></span>

<span data-ttu-id="da863-131">La machine virtuelle est désactivée lorsque la tâche d' **enregistrement** atteint son achèvement.</span><span class="sxs-lookup"><span data-stu-id="da863-131">The VM is turned off when the **Save** task reaches completion.</span></span> <span data-ttu-id="da863-132">La propriété [**IVMVirtualMachine :: State**](ivmvirtualmachine-state.md) contiendra les **vmVMState d' \_ enregistrement** pendant l’enregistrement, puis les **vmVMState \_ enregistrées** lorsque l’enregistrement est terminé et que la machine virtuelle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="da863-132">The [**IVMVirtualMachine::State**](ivmvirtualmachine-state.md) property will contain **vmVMState\_Saving** while the save is in progress, followed by **vmVMState\_Saved** when the save has completed and the VM is turned off.</span></span>

## <a name="requirements"></a><span data-ttu-id="da863-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da863-133">Requirements</span></span>



| <span data-ttu-id="da863-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da863-134">Requirement</span></span> | <span data-ttu-id="da863-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="da863-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da863-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da863-136">Minimum supported client</span></span><br/> | <span data-ttu-id="da863-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da863-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da863-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da863-138">Minimum supported server</span></span><br/> | <span data-ttu-id="da863-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="da863-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="da863-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="da863-140">End of client support</span></span><br/>    | <span data-ttu-id="da863-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="da863-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="da863-142">Produit</span><span class="sxs-lookup"><span data-stu-id="da863-142">Product</span></span><br/>                  | <span data-ttu-id="da863-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="da863-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="da863-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="da863-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="da863-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="da863-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="da863-146">IID</span><span class="sxs-lookup"><span data-stu-id="da863-146">IID</span></span><br/>                      | <span data-ttu-id="da863-147">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="da863-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="da863-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da863-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da863-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="da863-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

