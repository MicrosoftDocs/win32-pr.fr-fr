---
title: IVMVirtualMachine, méthode de reprise (VPCCOMInterfaces. h)
description: Reprend la machine virtuelle.
ms.assetid: 4a2d6b64-8dcf-484e-940d-b0180aba9f01
keywords:
- Reprendre la méthode Virtual PC
- Méthode de reprise Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Resume
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Resume
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c24af1e1a00aa0fa29acc077faf48287c0307414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844057"
---
# <a name="ivmvirtualmachineresume-method"></a><span data-ttu-id="61e8d-106">IVMVirtualMachine :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="61e8d-106">IVMVirtualMachine::Resume method</span></span>

<span data-ttu-id="61e8d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="61e8d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="61e8d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="61e8d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="61e8d-109">Reprend la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="61e8d-109">Resumes the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="61e8d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61e8d-110">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="61e8d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61e8d-111">Parameters</span></span>

<span data-ttu-id="61e8d-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="61e8d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61e8d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61e8d-113">Return value</span></span>

<span data-ttu-id="61e8d-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="61e8d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="61e8d-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="61e8d-115">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="61e8d-116">Description</span><span class="sxs-lookup"><span data-stu-id="61e8d-116">Description</span></span>                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61e8d-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="61e8d-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="61e8d-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="61e8d-119"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                                     | <span data-ttu-id="61e8d-120">La machine virtuelle n’est pas suspendue.</span><span class="sxs-lookup"><span data-stu-id="61e8d-120">The VM is not paused.</span></span><br/>                                              |
| <dl> <span data-ttu-id="61e8d-121">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="61e8d-122">L’appelant doit disposer des autorisations d’accès en exécution pour reprendre cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="61e8d-122">The caller must have execute access permissions to resume this VM.</span></span><br/> |
| <dl> <span data-ttu-id="61e8d-123"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-123"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="61e8d-124">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="61e8d-124">The operation did not complete in a timely manner.</span></span><br/>                 |
| <dl> <span data-ttu-id="61e8d-125"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-125"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="61e8d-126">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="61e8d-126">The VM is not running.</span></span><br/>                                             |
| <dl> <span data-ttu-id="61e8d-127"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="61e8d-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="61e8d-128">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="61e8d-128">The configuration is unknown.</span></span><br/>                                      |
| <dl> <span data-ttu-id="61e8d-129"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="61e8d-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="61e8d-130">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="61e8d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61e8d-131">Requirements</span></span>



| <span data-ttu-id="61e8d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61e8d-132">Requirement</span></span> | <span data-ttu-id="61e8d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="61e8d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e8d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61e8d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="61e8d-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61e8d-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61e8d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61e8d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="61e8d-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="61e8d-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="61e8d-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="61e8d-138">End of client support</span></span><br/>    | <span data-ttu-id="61e8d-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61e8d-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="61e8d-140">Produit</span><span class="sxs-lookup"><span data-stu-id="61e8d-140">Product</span></span><br/>                  | <span data-ttu-id="61e8d-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="61e8d-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="61e8d-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="61e8d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="61e8d-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="61e8d-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="61e8d-144">IID</span><span class="sxs-lookup"><span data-stu-id="61e8d-144">IID</span></span><br/>                      | <span data-ttu-id="61e8d-145">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="61e8d-145">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="61e8d-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61e8d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e8d-147">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="61e8d-147">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

