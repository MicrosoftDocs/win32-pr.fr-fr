---
title: IVMVirtualNetwork NetworkAdapters, propriété (VPCCOMInterfaces. h)
description: Récupère une collection énumérable de cartes réseau attachées au réseau virtuel.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- NetworkAdapters propriété Virtual PC
- NetworkAdapters, propriété Virtual PC, IVMVirtualNetwork, interface
- IVMVirtualNetwork interface Virtual PC, propriété NetworkAdapters
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba86f649744eeb34139c65de9aa4523ddc74d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511804"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a><span data-ttu-id="db44e-106">IVMVirtualNetwork :: NetworkAdapters, propriété</span><span class="sxs-lookup"><span data-stu-id="db44e-106">IVMVirtualNetwork::NetworkAdapters property</span></span>

<span data-ttu-id="db44e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="db44e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="db44e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="db44e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="db44e-109">Récupère une collection énumérable de cartes réseau attachées au réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="db44e-109">Retrieves an enumerable collection of NICs attached to the virtual network.</span></span>

<span data-ttu-id="db44e-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="db44e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db44e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db44e-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="db44e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="db44e-112">Property value</span></span>

<span data-ttu-id="db44e-113">Nouveau [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) qui contient les cartes réseau virtuelles attachées à ce réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="db44e-113">A new [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) which holds the virtual NICs attached to this virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db44e-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="db44e-114">Error codes</span></span>



| <span data-ttu-id="db44e-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="db44e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="db44e-116">Signification</span><span class="sxs-lookup"><span data-stu-id="db44e-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="db44e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="db44e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="db44e-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="db44e-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="db44e-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="db44e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="db44e-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="db44e-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="db44e-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="db44e-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="db44e-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="db44e-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="db44e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db44e-123">Requirements</span></span>



| <span data-ttu-id="db44e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db44e-124">Requirement</span></span> | <span data-ttu-id="db44e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="db44e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db44e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db44e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="db44e-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db44e-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db44e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db44e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="db44e-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="db44e-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="db44e-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="db44e-130">End of client support</span></span><br/>    | <span data-ttu-id="db44e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="db44e-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="db44e-132">Produit</span><span class="sxs-lookup"><span data-stu-id="db44e-132">Product</span></span><br/>                  | <span data-ttu-id="db44e-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="db44e-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="db44e-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="db44e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="db44e-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="db44e-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="db44e-136">IID</span><span class="sxs-lookup"><span data-stu-id="db44e-136">IID</span></span><br/>                      | <span data-ttu-id="db44e-137">IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="db44e-137">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="db44e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db44e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db44e-139">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="db44e-139">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

