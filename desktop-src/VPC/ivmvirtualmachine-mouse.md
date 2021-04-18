---
title: IVMVirtualMachine, propriété de souris (VPCCOMInterfaces. h)
description: Récupère le périphérique de la souris pour l’ordinateur virtuel.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Propriété de souris Virtual PC
- Propriété Mouse Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété Mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511805"
---
# <a name="ivmvirtualmachinemouse-property"></a><span data-ttu-id="527e3-106">IVMVirtualMachine :: Mouse, propriété</span><span class="sxs-lookup"><span data-stu-id="527e3-106">IVMVirtualMachine::Mouse property</span></span>

<span data-ttu-id="527e3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="527e3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="527e3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="527e3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="527e3-109">Récupère le périphérique de la souris pour l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="527e3-109">Retrieves the mouse device for the virtual machine.</span></span>

<span data-ttu-id="527e3-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="527e3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="527e3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="527e3-111">Syntax</span></span>


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a><span data-ttu-id="527e3-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="527e3-112">Property value</span></span>

<span data-ttu-id="527e3-113">Objet [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="527e3-113">An [**IVMMouse**](ivmmouse.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="527e3-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="527e3-114">Error codes</span></span>



| <span data-ttu-id="527e3-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="527e3-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="527e3-116">Signification</span><span class="sxs-lookup"><span data-stu-id="527e3-116">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="527e3-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="527e3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="527e3-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="527e3-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="527e3-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="527e3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="527e3-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="527e3-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="527e3-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="527e3-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="527e3-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="527e3-122">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="527e3-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="527e3-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="527e3-124">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="527e3-124">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="527e3-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="527e3-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="527e3-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="527e3-126">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="527e3-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="527e3-127">Requirements</span></span>



| <span data-ttu-id="527e3-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="527e3-128">Requirement</span></span> | <span data-ttu-id="527e3-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="527e3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="527e3-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="527e3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="527e3-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="527e3-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="527e3-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="527e3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="527e3-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="527e3-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="527e3-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="527e3-134">End of client support</span></span><br/>    | <span data-ttu-id="527e3-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="527e3-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="527e3-136">Produit</span><span class="sxs-lookup"><span data-stu-id="527e3-136">Product</span></span><br/>                  | <span data-ttu-id="527e3-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="527e3-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="527e3-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="527e3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="527e3-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="527e3-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="527e3-140">IID</span><span class="sxs-lookup"><span data-stu-id="527e3-140">IID</span></span><br/>                      | <span data-ttu-id="527e3-141">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="527e3-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="527e3-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="527e3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="527e3-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="527e3-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

