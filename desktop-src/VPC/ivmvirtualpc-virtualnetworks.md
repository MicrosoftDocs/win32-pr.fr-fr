---
title: IVMVirtualPC VirtualNetworks, propriété (VPCCOMInterfaces. h)
description: Récupère une collection énumérable de réseaux virtuels.
ms.assetid: 88c68178-0399-44cd-8145-1f2e4d6ac632
keywords:
- VirtualNetworks propriété Virtual PC
- VirtualNetworks, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété VirtualNetworks
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualNetworks
- IVMVirtualPC.get_VirtualNetworks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ea97a7d9bb65bb41842ca028ded88f9a26b63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106336"
---
# <a name="ivmvirtualpcvirtualnetworks-property"></a><span data-ttu-id="f0d8c-106">IVMVirtualPC :: VirtualNetworks, propriété</span><span class="sxs-lookup"><span data-stu-id="f0d8c-106">IVMVirtualPC::VirtualNetworks property</span></span>

<span data-ttu-id="f0d8c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f0d8c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f0d8c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f0d8c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f0d8c-109">Récupère une collection énumérable de réseaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="f0d8c-109">Retrieves an enumerable collection of virtual networks.</span></span>

<span data-ttu-id="f0d8c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f0d8c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d8c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0d8c-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetworks(
  [out, retval] IVMVirtualNetworkCollection **virtualNetworkCollection
);
```



## <a name="property-value"></a><span data-ttu-id="f0d8c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f0d8c-112">Property value</span></span>

<span data-ttu-id="f0d8c-113">Collection d’objets [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="f0d8c-113">A collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="f0d8c-114">Consultez [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span><span class="sxs-lookup"><span data-stu-id="f0d8c-114">See [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f0d8c-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f0d8c-115">Error codes</span></span>



| <span data-ttu-id="f0d8c-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f0d8c-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="f0d8c-117">Signification</span><span class="sxs-lookup"><span data-stu-id="f0d8c-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f0d8c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="f0d8c-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f0d8c-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f0d8c-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="f0d8c-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f0d8c-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="f0d8c-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8c-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="f0d8c-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f0d8c-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="f0d8c-124"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8c-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="f0d8c-125">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="f0d8c-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f0d8c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0d8c-126">Requirements</span></span>



| <span data-ttu-id="f0d8c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0d8c-127">Requirement</span></span> | <span data-ttu-id="f0d8c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0d8c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d8c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0d8c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d8c-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0d8c-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0d8c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0d8c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d8c-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0d8c-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f0d8c-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f0d8c-133">End of client support</span></span><br/>    | <span data-ttu-id="f0d8c-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f0d8c-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f0d8c-135">Produit</span><span class="sxs-lookup"><span data-stu-id="f0d8c-135">Product</span></span><br/>                  | <span data-ttu-id="f0d8c-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f0d8c-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f0d8c-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0d8c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d8c-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d8c-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f0d8c-139">IID</span><span class="sxs-lookup"><span data-stu-id="f0d8c-139">IID</span></span><br/>                      | <span data-ttu-id="f0d8c-140">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="f0d8c-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="f0d8c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0d8c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d8c-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="f0d8c-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

