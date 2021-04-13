---
title: IVMVirtualMachine, propriété annulable (VPCCOMInterfaces. h)
description: Détermine si les disques d’annulations sont activés pour les disques durs connectés à la machine virtuelle.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Propriété d’annulation de l’ordinateur virtuel
- Propriété d’annulation de l’ordinateur virtuel, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété Undo
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508626"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="421d2-106">IVMVirtualMachine :: Undoable, propriété</span><span class="sxs-lookup"><span data-stu-id="421d2-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="421d2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="421d2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="421d2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="421d2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="421d2-109">Détermine si les disques d’annulations sont activés pour les disques durs connectés à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="421d2-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="421d2-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="421d2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="421d2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="421d2-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="421d2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="421d2-112">Property value</span></span>

<span data-ttu-id="421d2-113">Spécifie la **\_ valeur variant true** si les lecteurs d’annulations sont activés pour les disques durs connectés à la machine virtuelle et la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="421d2-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="421d2-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="421d2-114">Error codes</span></span>



| <span data-ttu-id="421d2-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="421d2-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="421d2-116">Signification</span><span class="sxs-lookup"><span data-stu-id="421d2-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="421d2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="421d2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="421d2-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="421d2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="421d2-119"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="421d2-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="421d2-120">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="421d2-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="421d2-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="421d2-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="421d2-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="421d2-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="421d2-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="421d2-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="421d2-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="421d2-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="421d2-125"><dt>Ordinateur virtuel \_ E/r 0xA0040302 \_ \_ \_ active VM</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="421d2-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="421d2-126">La machine virtuelle est en cours d’exécution ou enregistrée.</span><span class="sxs-lookup"><span data-stu-id="421d2-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="421d2-127">Notes</span><span class="sxs-lookup"><span data-stu-id="421d2-127">Remarks</span></span>

<span data-ttu-id="421d2-128">Si les lecteurs d’annulations sont désactivés, tous les fichiers de lecteur d’annulation existants seront supprimés.</span><span class="sxs-lookup"><span data-stu-id="421d2-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="421d2-129">Vous ne pouvez pas définir cette propriété si la machine virtuelle est en cours d’exécution ou enregistrée.</span><span class="sxs-lookup"><span data-stu-id="421d2-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="421d2-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="421d2-130">Requirements</span></span>



| <span data-ttu-id="421d2-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="421d2-131">Requirement</span></span> | <span data-ttu-id="421d2-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="421d2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="421d2-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="421d2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="421d2-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="421d2-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="421d2-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="421d2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="421d2-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="421d2-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="421d2-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="421d2-137">End of client support</span></span><br/>    | <span data-ttu-id="421d2-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="421d2-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="421d2-139">Produit</span><span class="sxs-lookup"><span data-stu-id="421d2-139">Product</span></span><br/>                  | <span data-ttu-id="421d2-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="421d2-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="421d2-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="421d2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="421d2-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="421d2-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="421d2-143">IID</span><span class="sxs-lookup"><span data-stu-id="421d2-143">IID</span></span><br/>                      | <span data-ttu-id="421d2-144">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="421d2-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="421d2-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="421d2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421d2-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="421d2-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

