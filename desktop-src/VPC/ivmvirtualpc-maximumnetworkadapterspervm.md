---
title: IVMVirtualPC MaximumNetworkAdaptersPerVM, propriété (VPCCOMInterfaces. h)
description: Nombre maximal d’interfaces réseau par machine virtuelle.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- MaximumNetworkAdaptersPerVM propriété Virtual PC
- MaximumNetworkAdaptersPerVM, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété MaximumNetworkAdaptersPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0797775038440c566fa7a3397b05632af839a341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102793"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a><span data-ttu-id="0e14d-106">IVMVirtualPC :: MaximumNetworkAdaptersPerVM, propriété</span><span class="sxs-lookup"><span data-stu-id="0e14d-106">IVMVirtualPC::MaximumNetworkAdaptersPerVM property</span></span>

<span data-ttu-id="0e14d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0e14d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0e14d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0e14d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0e14d-109">Récupère le nombre maximal d’interfaces réseau par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e14d-109">Retrieves the maximum number of networks interfaces per virtual machine.</span></span>

<span data-ttu-id="0e14d-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0e14d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e14d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e14d-111">Syntax</span></span>


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a><span data-ttu-id="0e14d-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0e14d-112">Property value</span></span>

<span data-ttu-id="0e14d-113">Nombre maximal d’interfaces réseau par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0e14d-113">The maximum number of network interfaces per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0e14d-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0e14d-114">Error codes</span></span>



| <span data-ttu-id="0e14d-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="0e14d-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="0e14d-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0e14d-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e14d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e14d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="0e14d-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0e14d-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0e14d-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0e14d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="0e14d-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0e14d-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="0e14d-121"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="0e14d-121"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="0e14d-122">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="0e14d-122">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0e14d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e14d-123">Requirements</span></span>



| <span data-ttu-id="0e14d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e14d-124">Requirement</span></span> | <span data-ttu-id="0e14d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e14d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e14d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e14d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e14d-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e14d-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e14d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e14d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e14d-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e14d-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0e14d-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0e14d-130">End of client support</span></span><br/>    | <span data-ttu-id="0e14d-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e14d-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0e14d-132">Produit</span><span class="sxs-lookup"><span data-stu-id="0e14d-132">Product</span></span><br/>                  | <span data-ttu-id="0e14d-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0e14d-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0e14d-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e14d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e14d-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e14d-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0e14d-136">IID</span><span class="sxs-lookup"><span data-stu-id="0e14d-136">IID</span></span><br/>                      | <span data-ttu-id="0e14d-137">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="0e14d-137">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0e14d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e14d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e14d-139">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="0e14d-139">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

