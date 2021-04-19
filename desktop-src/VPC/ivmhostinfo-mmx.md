---
title: Propriété MMX IVMHostInfo (VPCCOMInterfaces. h)
description: Détermine si le processeur prend en charge le jeu d’instructions MMX. | Propriété MMX IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- MMX, propriété Virtual PC
- MMX, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e224ed6a0f15da9143a884dd1c1dfacc1634fce7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537215"
---
# <a name="ivmhostinfommx-property"></a><span data-ttu-id="7231f-107">IVMHostInfo :: MMX, propriété</span><span class="sxs-lookup"><span data-stu-id="7231f-107">IVMHostInfo::MMX property</span></span>

<span data-ttu-id="7231f-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7231f-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7231f-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7231f-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7231f-110">Détermine si le processeur prend en charge le jeu d’instructions MMX.</span><span class="sxs-lookup"><span data-stu-id="7231f-110">Determines whether the processor supports the MMX instruction set.</span></span>

<span data-ttu-id="7231f-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7231f-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7231f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7231f-112">Syntax</span></span>


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="7231f-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7231f-113">Property value</span></span>

<span data-ttu-id="7231f-114">**True** si les instructions MMX sont prises en charge ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="7231f-114">**TRUE** if MMX instructions are supported, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7231f-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7231f-115">Error codes</span></span>



| <span data-ttu-id="7231f-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7231f-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7231f-117">Signification</span><span class="sxs-lookup"><span data-stu-id="7231f-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7231f-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7231f-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7231f-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7231f-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7231f-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7231f-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7231f-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7231f-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7231f-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7231f-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7231f-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7231f-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7231f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7231f-124">Requirements</span></span>



| <span data-ttu-id="7231f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7231f-125">Requirement</span></span> | <span data-ttu-id="7231f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7231f-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7231f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7231f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7231f-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7231f-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7231f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7231f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7231f-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7231f-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7231f-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7231f-131">End of client support</span></span><br/>    | <span data-ttu-id="7231f-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7231f-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7231f-133">Produit</span><span class="sxs-lookup"><span data-stu-id="7231f-133">Product</span></span><br/>                  | <span data-ttu-id="7231f-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7231f-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7231f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7231f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7231f-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7231f-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7231f-137">IID</span><span class="sxs-lookup"><span data-stu-id="7231f-137">IID</span></span><br/>                      | <span data-ttu-id="7231f-138">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="7231f-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7231f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7231f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7231f-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="7231f-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

