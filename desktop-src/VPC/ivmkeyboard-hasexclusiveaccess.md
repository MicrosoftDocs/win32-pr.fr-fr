---
title: IVMKeyboard HasExclusiveAccess, propriété (VPCCOMInterfaces. h)
description: Indique si cet objet a un contrôle exclusif sur le périphérique clavier de la machine virtuelle.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- HasExclusiveAccess propriété Virtual PC
- HasExclusiveAccess, propriété Virtual PC, IVMKeyboard, interface
- IVMKeyboard interface Virtual PC, propriété HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105679"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="30a26-106">IVMKeyboard :: HasExclusiveAccess, propriété</span><span class="sxs-lookup"><span data-stu-id="30a26-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="30a26-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="30a26-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30a26-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30a26-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30a26-109">Indique si cet objet dispose d’un contrôle exclusif sur le périphérique clavier de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="30a26-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="30a26-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="30a26-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a26-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30a26-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="30a26-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="30a26-112">Property value</span></span>

<span data-ttu-id="30a26-113">**True** si l’accès exclusif au clavier de l’ordinateur virtuel a été acquis ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="30a26-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30a26-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="30a26-114">Error codes</span></span>



| <span data-ttu-id="30a26-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="30a26-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="30a26-116">Signification</span><span class="sxs-lookup"><span data-stu-id="30a26-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30a26-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="30a26-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="30a26-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="30a26-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="30a26-120">Le paramètre *isExclusive* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="30a26-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="30a26-121"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="30a26-122">Le mode exclusif demandé est déjà défini pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="30a26-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="30a26-123">Cela peut se produire lorsque vous tentez de définir le mode exclusif lorsqu’il a déjà été acquis, ou lorsque vous essayez de libérer le mode exclusif lorsqu’il n’a pas été acquis précédemment.</span><span class="sxs-lookup"><span data-stu-id="30a26-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="30a26-124"><dt>Ordinateur virtuel \_ Échec de la \_ définition du \_ \_ mode \_ exclusif</dt> <dt>0xA0040825</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="30a26-125">Échec de la définition ou de la libération du mode exclusif comme demandé.</span><span class="sxs-lookup"><span data-stu-id="30a26-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="30a26-126">Cela peut être dû au fait que la machine virtuelle n’est plus en cours d’exécution ou qu’un autre processus a déjà acquis le mode exclusif sur le périphérique clavier de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="30a26-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="30a26-127"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="30a26-128">La chaîne spécifiée est vide ou contient un code de clé non valide.</span><span class="sxs-lookup"><span data-stu-id="30a26-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="30a26-129"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="30a26-130">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="30a26-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="30a26-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30a26-131">Requirements</span></span>



| <span data-ttu-id="30a26-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30a26-132">Requirement</span></span> | <span data-ttu-id="30a26-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="30a26-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a26-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30a26-134">Minimum supported client</span></span><br/> | <span data-ttu-id="30a26-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30a26-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30a26-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30a26-136">Minimum supported server</span></span><br/> | <span data-ttu-id="30a26-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="30a26-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="30a26-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="30a26-138">End of client support</span></span><br/>    | <span data-ttu-id="30a26-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30a26-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="30a26-140">Produit</span><span class="sxs-lookup"><span data-stu-id="30a26-140">Product</span></span><br/>                  | <span data-ttu-id="30a26-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="30a26-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="30a26-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="30a26-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="30a26-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="30a26-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="30a26-144">IID</span><span class="sxs-lookup"><span data-stu-id="30a26-144">IID</span></span><br/>                      | <span data-ttu-id="30a26-145">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="30a26-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="30a26-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30a26-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a26-147">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="30a26-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

