---
title: IVMVirtualMachine pause, méthode (VPCCOMInterfaces. h)
description: Suspend la machine virtuelle.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Suspendre la méthode Virtual PC
- Suspendre la méthode Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, pause, méthode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c953da05d34c999066a6bc87cb1f51983defbd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843945"
---
# <a name="ivmvirtualmachinepause-method"></a><span data-ttu-id="7a6db-106">IVMVirtualMachine ::P méthode ause</span><span class="sxs-lookup"><span data-stu-id="7a6db-106">IVMVirtualMachine::Pause method</span></span>

<span data-ttu-id="7a6db-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a6db-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a6db-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a6db-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a6db-109">Suspend la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7a6db-109">Pauses the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6db-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a6db-110">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="7a6db-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a6db-111">Parameters</span></span>

<span data-ttu-id="7a6db-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7a6db-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a6db-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a6db-113">Return value</span></span>

<span data-ttu-id="7a6db-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7a6db-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7a6db-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7a6db-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="7a6db-116">Description</span><span class="sxs-lookup"><span data-stu-id="7a6db-116">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a6db-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="7a6db-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7a6db-118">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7a6db-119"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="7a6db-120">La machine virtuelle est déjà suspendue.</span><span class="sxs-lookup"><span data-stu-id="7a6db-120">The VM is already paused.</span></span><br/>                                         |
| <dl> <span data-ttu-id="7a6db-121">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="7a6db-122">L’appelant doit avoir des autorisations d’accès en exécution pour suspendre cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7a6db-122">The caller must have execute access permissions to pause this VM.</span></span><br/> |
| <dl> <span data-ttu-id="7a6db-123"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="7a6db-124">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="7a6db-124">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="7a6db-125"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="7a6db-126">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7a6db-126">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="7a6db-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="7a6db-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="7a6db-128">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="7a6db-128">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7a6db-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="7a6db-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7a6db-130">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="7a6db-131">Notes</span><span class="sxs-lookup"><span data-stu-id="7a6db-131">Remarks</span></span>

<span data-ttu-id="7a6db-132">La **suspension** n’enregistre pas l’état actuel de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7a6db-132">**Pause** does not save the current state of the VM.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a6db-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a6db-133">Requirements</span></span>



| <span data-ttu-id="7a6db-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a6db-134">Requirement</span></span> | <span data-ttu-id="7a6db-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a6db-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6db-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a6db-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7a6db-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a6db-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a6db-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a6db-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7a6db-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a6db-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a6db-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7a6db-140">End of client support</span></span><br/>    | <span data-ttu-id="7a6db-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a6db-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a6db-142">Produit</span><span class="sxs-lookup"><span data-stu-id="7a6db-142">Product</span></span><br/>                  | <span data-ttu-id="7a6db-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a6db-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a6db-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a6db-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a6db-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a6db-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7a6db-146">IID</span><span class="sxs-lookup"><span data-stu-id="7a6db-146">IID</span></span><br/>                      | <span data-ttu-id="7a6db-147">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="7a6db-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7a6db-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a6db-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6db-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="7a6db-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

