---
title: Propriété notes IVMVirtualMachine (VPCCOMInterfaces. h)
description: Remarques relatives à la machine virtuelle.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Propriété notes Virtual PC
- Propriété notes Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété notes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466618"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="6db47-106">IVMVirtualMachine :: notes, propriété</span><span class="sxs-lookup"><span data-stu-id="6db47-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="6db47-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6db47-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6db47-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6db47-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6db47-109">Récupère et définit les notes pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6db47-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="6db47-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6db47-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db47-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6db47-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="6db47-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6db47-112">Property value</span></span>

<span data-ttu-id="6db47-113">Spécifie les remarques pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="6db47-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="6db47-114">La longueur maximale de la chaîne est de 65 536 caractères.</span><span class="sxs-lookup"><span data-stu-id="6db47-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="6db47-115">Pour supprimer des notes, transmettez une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="6db47-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6db47-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6db47-116">Error codes</span></span>



| <span data-ttu-id="6db47-117">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="6db47-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6db47-118">Signification</span><span class="sxs-lookup"><span data-stu-id="6db47-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6db47-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6db47-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6db47-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6db47-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="6db47-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6db47-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6db47-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6db47-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="6db47-123"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6db47-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="6db47-124">Le paramètre n’est pas valide ou contient plus de 65 536 caractères.</span><span class="sxs-lookup"><span data-stu-id="6db47-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="6db47-125"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="6db47-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="6db47-126">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="6db47-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="6db47-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6db47-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6db47-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6db47-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="6db47-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6db47-129">Requirements</span></span>



| <span data-ttu-id="6db47-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6db47-130">Requirement</span></span> | <span data-ttu-id="6db47-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6db47-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db47-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6db47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6db47-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6db47-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6db47-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6db47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6db47-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6db47-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6db47-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6db47-136">End of client support</span></span><br/>    | <span data-ttu-id="6db47-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6db47-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6db47-138">Produit</span><span class="sxs-lookup"><span data-stu-id="6db47-138">Product</span></span><br/>                  | <span data-ttu-id="6db47-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6db47-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6db47-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="6db47-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db47-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db47-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6db47-142">IID</span><span class="sxs-lookup"><span data-stu-id="6db47-142">IID</span></span><br/>                      | <span data-ttu-id="6db47-143">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="6db47-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6db47-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6db47-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db47-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="6db47-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

