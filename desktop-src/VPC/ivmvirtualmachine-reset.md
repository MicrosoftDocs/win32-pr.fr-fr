---
title: Méthode de réinitialisation IVMVirtualMachine (VPCCOMInterfaces. h)
description: Réinitialise l’ordinateur virtuel.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Réinitialiser la méthode Virtual PC
- Réinitialiser la méthode Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode Reset
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45314eef6d837ac00647d477f3652b63221d977c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466394"
---
# <a name="ivmvirtualmachinereset-method"></a><span data-ttu-id="314ad-106">IVMVirtualMachine :: Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="314ad-106">IVMVirtualMachine::Reset method</span></span>

<span data-ttu-id="314ad-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="314ad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="314ad-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="314ad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="314ad-109">Réinitialise l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="314ad-109">Resets the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="314ad-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="314ad-110">Syntax</span></span>


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a><span data-ttu-id="314ad-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="314ad-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314ad-112">*resetTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="314ad-112">*resetTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="314ad-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de réinitialisation de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="314ad-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the VM's reset sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314ad-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="314ad-114">Return value</span></span>

<span data-ttu-id="314ad-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="314ad-115">This method can return one of these values.</span></span>



| <span data-ttu-id="314ad-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="314ad-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="314ad-117">Description</span><span class="sxs-lookup"><span data-stu-id="314ad-117">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="314ad-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="314ad-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="314ad-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="314ad-119">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="314ad-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="314ad-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="314ad-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="314ad-121">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="314ad-122">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="314ad-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="314ad-123">L’appelant doit disposer des autorisations d’accès en exécution pour réinitialiser cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="314ad-123">The caller must have execute access permissions to reset this VM.</span></span><br/> |
| <dl> <span data-ttu-id="314ad-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="314ad-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="314ad-125">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="314ad-125">The VM is not running.</span></span><br/>                                            |
| <dl> <span data-ttu-id="314ad-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="314ad-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="314ad-127">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="314ad-127">The configuration is unknown.</span></span><br/>                                     |
| <dl> <span data-ttu-id="314ad-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="314ad-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="314ad-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="314ad-129">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="314ad-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="314ad-130">Requirements</span></span>



| <span data-ttu-id="314ad-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="314ad-131">Requirement</span></span> | <span data-ttu-id="314ad-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="314ad-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="314ad-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="314ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="314ad-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="314ad-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="314ad-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="314ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="314ad-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="314ad-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="314ad-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="314ad-137">End of client support</span></span><br/>    | <span data-ttu-id="314ad-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="314ad-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="314ad-139">Produit</span><span class="sxs-lookup"><span data-stu-id="314ad-139">Product</span></span><br/>                  | <span data-ttu-id="314ad-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="314ad-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="314ad-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="314ad-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="314ad-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="314ad-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="314ad-143">IID</span><span class="sxs-lookup"><span data-stu-id="314ad-143">IID</span></span><br/>                      | <span data-ttu-id="314ad-144">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="314ad-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="314ad-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="314ad-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314ad-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="314ad-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

