---
title: Méthode IVMVirtualMachine TurnOff (VPCCOMInterfaces. h)
description: Met l’ordinateur virtuel hors tension.
ms.assetid: 4ea00314-8f1e-47d9-bbb8-b5791af1fb86
keywords:
- Méthode TurnOff Virtual PC
- Méthode TurnOff Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode TurnOff
topic_type:
- apiref
api_name:
- IVMVirtualMachine.TurnOff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27a5b14955fcc8a060c49932e3fa4f238497a567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033118"
---
# <a name="ivmvirtualmachineturnoff-method"></a><span data-ttu-id="dffa3-106">IVMVirtualMachine :: TurnOff, méthode</span><span class="sxs-lookup"><span data-stu-id="dffa3-106">IVMVirtualMachine::TurnOff method</span></span>

<span data-ttu-id="dffa3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dffa3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dffa3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dffa3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dffa3-109">Met l’ordinateur virtuel hors tension.</span><span class="sxs-lookup"><span data-stu-id="dffa3-109">Turns off the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="dffa3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dffa3-110">Syntax</span></span>


```C++
HRESULT TurnOff(
  [out, retval] IVMTask **turnOffTask
);
```



## <a name="parameters"></a><span data-ttu-id="dffa3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dffa3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dffa3-112">*turnOffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dffa3-112">*turnOffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dffa3-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence turnoff de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dffa3-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the virtual machine's turnoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dffa3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dffa3-114">Return value</span></span>

<span data-ttu-id="dffa3-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="dffa3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="dffa3-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dffa3-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="dffa3-117">Description</span><span class="sxs-lookup"><span data-stu-id="dffa3-117">Description</span></span>                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dffa3-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dffa3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="dffa3-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="dffa3-119">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="dffa3-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="dffa3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="dffa3-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="dffa3-121">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dffa3-122">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="dffa3-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="dffa3-123">L’appelant doit disposer des autorisations d’accès en exécution pour désactiver cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="dffa3-123">The caller must have execute access permissions to turn off this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="dffa3-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="dffa3-124"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="dffa3-125">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="dffa3-125">The virtual machine is not running.</span></span><br/>                                               |
| <dl> <span data-ttu-id="dffa3-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="dffa3-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="dffa3-127">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="dffa3-127">The configuration is unknown.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="dffa3-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="dffa3-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="dffa3-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="dffa3-129">An unexpected error has occurred.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="dffa3-130">Notes</span><span class="sxs-lookup"><span data-stu-id="dffa3-130">Remarks</span></span>

<span data-ttu-id="dffa3-131">Cette méthode désactive l’ordinateur virtuel de la même façon que la mise hors tension d’un ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="dffa3-131">This method turns off the virtual machine in the same manner as turning the power off on a physical machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="dffa3-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dffa3-132">Requirements</span></span>



| <span data-ttu-id="dffa3-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dffa3-133">Requirement</span></span> | <span data-ttu-id="dffa3-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="dffa3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dffa3-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dffa3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dffa3-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dffa3-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dffa3-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dffa3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dffa3-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dffa3-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dffa3-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dffa3-139">End of client support</span></span><br/>    | <span data-ttu-id="dffa3-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dffa3-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dffa3-141">Produit</span><span class="sxs-lookup"><span data-stu-id="dffa3-141">Product</span></span><br/>                  | <span data-ttu-id="dffa3-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dffa3-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dffa3-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="dffa3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dffa3-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dffa3-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dffa3-145">IID</span><span class="sxs-lookup"><span data-stu-id="dffa3-145">IID</span></span><br/>                      | <span data-ttu-id="dffa3-146">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="dffa3-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dffa3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dffa3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dffa3-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="dffa3-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

