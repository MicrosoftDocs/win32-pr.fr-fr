---
title: IVMVirtualMachineCollection, propriété d’élément (VPCCOMInterfaces. h)
description: Récupère l’objet ordinateur virtuel qui correspond à l’index spécifié.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Propriété de l’élément Virtual PC
- Propriété d’élément Virtual PC, interface IVMVirtualMachineCollection
- IVMVirtualMachineCollection interface Virtual PC, propriété Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032294"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a><span data-ttu-id="89751-106">IVMVirtualMachineCollection :: Item, propriété</span><span class="sxs-lookup"><span data-stu-id="89751-106">IVMVirtualMachineCollection::Item property</span></span>

<span data-ttu-id="89751-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="89751-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89751-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89751-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89751-109">Récupère l’objet ordinateur virtuel qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="89751-109">Retrieves the virtual machine object that corresponds to the specified index.</span></span>

<span data-ttu-id="89751-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="89751-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89751-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89751-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="89751-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="89751-112">Property value</span></span>

<span data-ttu-id="89751-113">Objet [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="89751-113">The [**IVMVirtualMachine**](ivmvirtualmachine.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89751-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="89751-114">Error codes</span></span>



| <span data-ttu-id="89751-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="89751-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="89751-116">Signification</span><span class="sxs-lookup"><span data-stu-id="89751-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89751-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89751-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="89751-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="89751-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="89751-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="89751-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="89751-120">Le paramètre *VirtualMachine* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="89751-120">The *virtualMachine* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="89751-121"><dt>DISP \_ \_BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="89751-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="89751-122">L’index de l’élément demandé ne correspond pas à un élément de cette collection.</span><span class="sxs-lookup"><span data-stu-id="89751-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="89751-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="89751-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="89751-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="89751-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="89751-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89751-125">Requirements</span></span>



| <span data-ttu-id="89751-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89751-126">Requirement</span></span> | <span data-ttu-id="89751-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="89751-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89751-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89751-128">Minimum supported client</span></span><br/> | <span data-ttu-id="89751-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89751-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89751-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89751-130">Minimum supported server</span></span><br/> | <span data-ttu-id="89751-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="89751-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="89751-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="89751-132">End of client support</span></span><br/>    | <span data-ttu-id="89751-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89751-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="89751-134">Produit</span><span class="sxs-lookup"><span data-stu-id="89751-134">Product</span></span><br/>                  | <span data-ttu-id="89751-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89751-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="89751-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="89751-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="89751-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="89751-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="89751-138">IID</span><span class="sxs-lookup"><span data-stu-id="89751-138">IID</span></span><br/>                      | <span data-ttu-id="89751-139">IID \_ IVMVirtualMachineCollection est défini en tant que 59f31786-2a3d-4FBF-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="89751-139">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89751-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89751-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89751-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="89751-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="89751-142">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="89751-142">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

