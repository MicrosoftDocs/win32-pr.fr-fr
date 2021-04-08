---
title: IVMVirtualMachine HasMMX, propriété (VPCCOMInterfaces. h)
description: Détermine si le processeur prend en charge le jeu d’instructions MMX. | IVMVirtualMachine HasMMX, propriété (VPCCOMInterfaces. h)
ms.assetid: 85350abe-ab44-42d2-9f3e-0fbdb64ff854
keywords:
- HasMMX propriété Virtual PC
- HasMMX, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété HasMMX
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasMMX
- IVMVirtualMachine.get_HasMMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e6b780d14749db193b2a7ce9a41083c6bf7031
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043066"
---
# <a name="ivmvirtualmachinehasmmx-property"></a><span data-ttu-id="0eef1-107">IVMVirtualMachine :: HasMMX, propriété</span><span class="sxs-lookup"><span data-stu-id="0eef1-107">IVMVirtualMachine::HasMMX property</span></span>

<span data-ttu-id="0eef1-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0eef1-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0eef1-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0eef1-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0eef1-110">Détermine si le processeur prend en charge le jeu d’instructions MMX.</span><span class="sxs-lookup"><span data-stu-id="0eef1-110">Determines whether the processor supports the MMX instruction set.</span></span>

<span data-ttu-id="0eef1-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0eef1-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eef1-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0eef1-112">Syntax</span></span>


```C++
HRESULT get_HasMMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="0eef1-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0eef1-113">Property value</span></span>

<span data-ttu-id="0eef1-114">**True** si le processeur prend en charge le jeu d’instructions MMX ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="0eef1-114">**TRUE** if the processor supported the MMX instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0eef1-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0eef1-115">Error codes</span></span>



| <span data-ttu-id="0eef1-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="0eef1-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0eef1-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0eef1-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0eef1-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0eef1-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0eef1-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0eef1-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0eef1-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0eef1-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0eef1-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0eef1-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0eef1-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="0eef1-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="0eef1-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="0eef1-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="0eef1-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0eef1-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0eef1-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0eef1-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0eef1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0eef1-126">Requirements</span></span>



| <span data-ttu-id="0eef1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0eef1-127">Requirement</span></span> | <span data-ttu-id="0eef1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0eef1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eef1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eef1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0eef1-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0eef1-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0eef1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eef1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0eef1-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eef1-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0eef1-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0eef1-133">End of client support</span></span><br/>    | <span data-ttu-id="0eef1-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0eef1-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0eef1-135">Produit</span><span class="sxs-lookup"><span data-stu-id="0eef1-135">Product</span></span><br/>                  | <span data-ttu-id="0eef1-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0eef1-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0eef1-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="0eef1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eef1-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eef1-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0eef1-139">IID</span><span class="sxs-lookup"><span data-stu-id="0eef1-139">IID</span></span><br/>                      | <span data-ttu-id="0eef1-140">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0eef1-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0eef1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eef1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eef1-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="0eef1-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

