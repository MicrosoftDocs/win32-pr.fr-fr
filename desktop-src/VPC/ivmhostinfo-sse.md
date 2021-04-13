---
title: IVMHostInfo SSE, propriété (VPCCOMInterfaces. h)
description: Détermine si le processeur prend en charge le jeu d’instructions SSE. | IVMHostInfo SSE, propriété (VPCCOMInterfaces. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- Virtual PC de la propriété SSE
- SSE, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété SSE
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322369"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="eeb04-107">IVMHostInfo :: SSE, propriété</span><span class="sxs-lookup"><span data-stu-id="eeb04-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="eeb04-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eeb04-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eeb04-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eeb04-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eeb04-110">Détermine si le processeur prend en charge le jeu d’instructions SSE.</span><span class="sxs-lookup"><span data-stu-id="eeb04-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="eeb04-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eeb04-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb04-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eeb04-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="eeb04-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eeb04-113">Property value</span></span>

<span data-ttu-id="eeb04-114">**True** si les instructions SSE sont prises en charge par le processeur hôte ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="eeb04-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eeb04-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eeb04-115">Error codes</span></span>



| <span data-ttu-id="eeb04-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="eeb04-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="eeb04-117">Signification</span><span class="sxs-lookup"><span data-stu-id="eeb04-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="eeb04-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eeb04-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="eeb04-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="eeb04-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="eeb04-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="eeb04-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="eeb04-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="eeb04-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="eeb04-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="eeb04-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="eeb04-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="eeb04-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eeb04-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeb04-124">Requirements</span></span>



| <span data-ttu-id="eeb04-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeb04-125">Requirement</span></span> | <span data-ttu-id="eeb04-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeb04-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb04-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb04-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb04-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeb04-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eeb04-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb04-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb04-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb04-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eeb04-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="eeb04-131">End of client support</span></span><br/>    | <span data-ttu-id="eeb04-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eeb04-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eeb04-133">Produit</span><span class="sxs-lookup"><span data-stu-id="eeb04-133">Product</span></span><br/>                  | <span data-ttu-id="eeb04-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eeb04-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eeb04-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="eeb04-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeb04-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeb04-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eeb04-137">IID</span><span class="sxs-lookup"><span data-stu-id="eeb04-137">IID</span></span><br/>                      | <span data-ttu-id="eeb04-138">IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="eeb04-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="eeb04-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeb04-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb04-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="eeb04-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

