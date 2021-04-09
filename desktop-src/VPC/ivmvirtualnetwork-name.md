---
title: Propriété IVMVirtualNetwork Name (VPCCOMInterfaces. h)
description: Nom unique de l’instance de réseau virtuel.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Propriété de nom Virtual PC
- Propriété de nom Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface Virtual PC, propriété Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942679"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="4df46-106">IVMVirtualNetwork :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="4df46-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="4df46-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4df46-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4df46-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4df46-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4df46-109">Récupère le nom unique de l’instance de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="4df46-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="4df46-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4df46-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df46-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4df46-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="4df46-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4df46-112">Property value</span></span>

<span data-ttu-id="4df46-113">nom du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="4df46-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4df46-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4df46-114">Error codes</span></span>



| <span data-ttu-id="4df46-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="4df46-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4df46-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4df46-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4df46-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4df46-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4df46-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4df46-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="4df46-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4df46-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4df46-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4df46-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="4df46-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4df46-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4df46-122">Une erreur inattendue s’est produite ou l’instance de réseau virtuel est inconnue.</span><span class="sxs-lookup"><span data-stu-id="4df46-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4df46-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4df46-123">Remarks</span></span>

<span data-ttu-id="4df46-124">Les noms de réseaux virtuels ne respectent pas la casse, par exemple, « MyNetwork » et « mynetwork » font référence au même réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="4df46-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df46-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4df46-125">Requirements</span></span>



| <span data-ttu-id="4df46-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4df46-126">Requirement</span></span> | <span data-ttu-id="4df46-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4df46-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df46-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df46-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4df46-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4df46-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4df46-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df46-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4df46-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4df46-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4df46-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4df46-132">End of client support</span></span><br/>    | <span data-ttu-id="4df46-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4df46-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4df46-134">Produit</span><span class="sxs-lookup"><span data-stu-id="4df46-134">Product</span></span><br/>                  | <span data-ttu-id="4df46-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4df46-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4df46-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="4df46-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4df46-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df46-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4df46-138">IID</span><span class="sxs-lookup"><span data-stu-id="4df46-138">IID</span></span><br/>                      | <span data-ttu-id="4df46-139">IID \_ IVMVirtualNetwork est défini en tant que 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="4df46-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4df46-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4df46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df46-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="4df46-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

