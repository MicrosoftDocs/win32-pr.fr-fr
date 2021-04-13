---
title: IVMVirtualMachine UndoAction, propriété (VPCCOMInterfaces. h)
description: Action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est arrêtée.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- UndoAction, propriété Virtual PC
- UndoAction, propriété Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, UndoAction, propriété
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466378"
---
# <a name="ivmvirtualmachineundoaction-property"></a><span data-ttu-id="b7693-106">IVMVirtualMachine :: UndoAction, propriété</span><span class="sxs-lookup"><span data-stu-id="b7693-106">IVMVirtualMachine::UndoAction property</span></span>

<span data-ttu-id="b7693-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b7693-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7693-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b7693-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7693-109">Récupère et définit l’action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est désactivée à l’aide de la méthode [**turnoff**](ivmvirtualmachine-turnoff.md) ou qu’elle est arrêtée à l’aide de la méthode [**Shutdown**](ivmguestos-shutdown.md) ou désactivée dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="b7693-109">Retrieves and sets the default action to be performed on all undo drives when the virtual machine (VM) is turned off using the [**TurnOff**](ivmvirtualmachine-turnoff.md) method or shut down using the [**Shutdown**](ivmguestos-shutdown.md) method or turned off from within the guest operating system.</span></span>

<span data-ttu-id="b7693-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b7693-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7693-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7693-111">Syntax</span></span>


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a><span data-ttu-id="b7693-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b7693-112">Property value</span></span>

<span data-ttu-id="b7693-113">Spécifie l’action par défaut à effectuer sur tous les lecteurs d’annulation lorsque la machine virtuelle est arrêtée depuis le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="b7693-113">Specifies the default action to be performed on all undo drives when the VM is shut down from within the guest operating system.</span></span> <span data-ttu-id="b7693-114">Pour obtenir la liste des valeurs, consultez [**VMUndoAction**](vmundoaction.md).</span><span class="sxs-lookup"><span data-stu-id="b7693-114">For a list of values, see [**VMUndoAction**](vmundoaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="b7693-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b7693-115">Error codes</span></span>



| <span data-ttu-id="b7693-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="b7693-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b7693-117">Signification</span><span class="sxs-lookup"><span data-stu-id="b7693-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b7693-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b7693-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b7693-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b7693-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b7693-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b7693-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b7693-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b7693-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b7693-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b7693-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="b7693-123">Ce paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b7693-123">The parameter is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="b7693-124"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="b7693-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b7693-125">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="b7693-125">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b7693-126"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b7693-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b7693-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b7693-127">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b7693-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7693-128">Requirements</span></span>



| <span data-ttu-id="b7693-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7693-129">Requirement</span></span> | <span data-ttu-id="b7693-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7693-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7693-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7693-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b7693-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7693-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7693-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7693-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b7693-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7693-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7693-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b7693-135">End of client support</span></span><br/>    | <span data-ttu-id="b7693-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7693-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7693-137">Produit</span><span class="sxs-lookup"><span data-stu-id="b7693-137">Product</span></span><br/>                  | <span data-ttu-id="b7693-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7693-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7693-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7693-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7693-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7693-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b7693-141">IID</span><span class="sxs-lookup"><span data-stu-id="b7693-141">IID</span></span><br/>                      | <span data-ttu-id="b7693-142">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b7693-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b7693-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7693-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7693-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b7693-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

