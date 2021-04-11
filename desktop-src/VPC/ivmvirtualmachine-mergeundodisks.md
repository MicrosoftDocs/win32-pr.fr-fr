---
title: Méthode IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Fusionne les disques d’annulations virtuelles.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- Méthode MergeUndoDisks Virtual PC
- Méthode MergeUndoDisks Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317402"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a><span data-ttu-id="c5e52-106">IVMVirtualMachine :: MergeUndoDisks, méthode</span><span class="sxs-lookup"><span data-stu-id="c5e52-106">IVMVirtualMachine::MergeUndoDisks method</span></span>

<span data-ttu-id="c5e52-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c5e52-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c5e52-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c5e52-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c5e52-109">Fusionne les disques d’annulations virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c5e52-109">Merges the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e52-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5e52-110">Syntax</span></span>


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="c5e52-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5e52-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e52-112">*undoMergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c5e52-112">*undoMergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e52-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la création de l’image.</span><span class="sxs-lookup"><span data-stu-id="c5e52-113">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e52-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5e52-114">Return value</span></span>

<span data-ttu-id="c5e52-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c5e52-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c5e52-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c5e52-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="c5e52-117">Description</span><span class="sxs-lookup"><span data-stu-id="c5e52-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5e52-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="c5e52-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c5e52-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c5e52-120"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="c5e52-121">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c5e52-121">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="c5e52-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="c5e52-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c5e52-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="c5e52-124">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="c5e52-125">Le système ne peut pas trouver le chemin d’accès spécifié par le paramètre *convertedDiskImagePath* ou l’un des disques parents n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c5e52-125">The system cannot find the path specified by the *convertedDiskImagePath* parameter or one of the parent disks is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c5e52-126"><dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-126"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                               | <span data-ttu-id="c5e52-127">L’utilisateur actuel ne dispose pas d’un accès suffisant au fichier parent.</span><span class="sxs-lookup"><span data-stu-id="c5e52-127">The current user has insufficient access to the parent file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="c5e52-128"><dt>**E \_ HANDLE**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-128"><dt>**E\_HANDLE**</dt> <dt>0x80070006</dt></span></span> </dl>                                     | <span data-ttu-id="c5e52-129">Un des disques parents est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c5e52-129">One of the parent disks is in use.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="c5e52-130"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="c5e52-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="c5e52-131">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="c5e52-131">The configuration is unknown.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c5e52-132"><dt>**Ordinateur virtuel \_ \_Machine virtuelle E \_ exécutant**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-132"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                            | <span data-ttu-id="c5e52-133">La machine virtuelle est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c5e52-133">The virtual machine is running.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="c5e52-134"><dt>**Ordinateur virtuel \_ \_Fichier E \_ lecture \_ seule**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-134"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                       | <span data-ttu-id="c5e52-135">Le parent des disques d’annulations virtuelles est marqué en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c5e52-135">The parent of virtual undo disks is marked as read only.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="c5e52-136"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="c5e52-137">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c5e52-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c5e52-138">Notes</span><span class="sxs-lookup"><span data-stu-id="c5e52-138">Remarks</span></span>

<span data-ttu-id="c5e52-139">**MergeUndoDisks** ne peut pas être appelé tant que l’ordinateur virtuel est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c5e52-139">**MergeUndoDisks** cannot be called while the virtual machine is still running.</span></span> <span data-ttu-id="c5e52-140">Utilisez [**IVMVirtualMachine :: Save**](ivmvirtualmachine-save.md) pour enregistrer l’état de l’ordinateur virtuel avant d’appeler **MergeUndoDisks** ou [**IVMVirtualMachine :: turnoff**](ivmvirtualmachine-turnoff.md) pour désactiver l’ordinateur virtuel sans enregistrer préalablement son état actuel.</span><span class="sxs-lookup"><span data-stu-id="c5e52-140">Use [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md) to save the state of the virtual machine before calling **MergeUndoDisks**, or [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md) to turn off the virtual machine without saving its current state beforehand.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e52-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5e52-141">Requirements</span></span>



| <span data-ttu-id="c5e52-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5e52-142">Requirement</span></span> | <span data-ttu-id="c5e52-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5e52-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e52-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5e52-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e52-145">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5e52-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5e52-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5e52-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e52-147">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5e52-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c5e52-148">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c5e52-148">End of client support</span></span><br/>    | <span data-ttu-id="c5e52-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5e52-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c5e52-150">Produit</span><span class="sxs-lookup"><span data-stu-id="c5e52-150">Product</span></span><br/>                  | <span data-ttu-id="c5e52-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c5e52-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c5e52-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5e52-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e52-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e52-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c5e52-154">IID</span><span class="sxs-lookup"><span data-stu-id="c5e52-154">IID</span></span><br/>                      | <span data-ttu-id="c5e52-155">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c5e52-155">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c5e52-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5e52-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e52-157">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="c5e52-157">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

