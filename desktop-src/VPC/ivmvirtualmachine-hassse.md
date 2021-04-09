---
title: IVMVirtualMachine HasSSE, propriété (VPCCOMInterfaces. h)
description: Détermine si le processeur prend en charge le jeu d’instructions SSE. | IVMVirtualMachine HasSSE, propriété (VPCCOMInterfaces. h)
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- HasSSE propriété Virtual PC
- HasSSE, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété HasSSE
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103870022"
---
# <a name="ivmvirtualmachinehassse-property"></a><span data-ttu-id="3e743-107">IVMVirtualMachine :: HasSSE, propriété</span><span class="sxs-lookup"><span data-stu-id="3e743-107">IVMVirtualMachine::HasSSE property</span></span>

<span data-ttu-id="3e743-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e743-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e743-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e743-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e743-110">Détermine si le processeur prend en charge le jeu d’instructions SSE.</span><span class="sxs-lookup"><span data-stu-id="3e743-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="3e743-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e743-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e743-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e743-112">Syntax</span></span>


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="3e743-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3e743-113">Property value</span></span>

<span data-ttu-id="3e743-114">**True** si le processeur prend en charge le jeu d’instructions SSE, sinon **false** .</span><span class="sxs-lookup"><span data-stu-id="3e743-114">**TRUE** if the processor supported the SSE instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e743-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3e743-115">Error codes</span></span>



| <span data-ttu-id="3e743-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="3e743-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3e743-117">Signification</span><span class="sxs-lookup"><span data-stu-id="3e743-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e743-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e743-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3e743-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3e743-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3e743-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3e743-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3e743-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3e743-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3e743-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3e743-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3e743-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="3e743-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="3e743-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3e743-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3e743-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3e743-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3e743-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e743-126">Requirements</span></span>



| <span data-ttu-id="3e743-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e743-127">Requirement</span></span> | <span data-ttu-id="3e743-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e743-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e743-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e743-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3e743-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e743-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e743-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e743-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3e743-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e743-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e743-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3e743-133">End of client support</span></span><br/>    | <span data-ttu-id="3e743-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e743-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e743-135">Produit</span><span class="sxs-lookup"><span data-stu-id="3e743-135">Product</span></span><br/>                  | <span data-ttu-id="3e743-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e743-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e743-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e743-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e743-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e743-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e743-139">IID</span><span class="sxs-lookup"><span data-stu-id="3e743-139">IID</span></span><br/>                      | <span data-ttu-id="3e743-140">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3e743-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3e743-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e743-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e743-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3e743-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

